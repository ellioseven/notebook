# Workers

### Code

```javascript
// main.js

const { Worker } = require("worker_threads")

const n = process.argv[2] || 5000000000

const runService = (workerData) => {
  return new Promise((resolve, reject) => {
    const worker = new Worker("./worker.js", {
      workerData
    })

    worker.on("message", resolve)
    worker.on("error", reject)
    worker.on("exit", (code) => {
      if (code !== 0) {
        reject(new Error(`Worker stopped with exit code ${code}`))
      }
    })
  })
}

const run = async () => {
  let timer = 0
  
  const interval = setInterval(() => {
    timer++
    console.log(`[${timer}s] Workers are working...`)
  }, 1000)

  const result = await Promise.all([
    runService({ n: +n }),
    runService({ n: +n })
  ])

  clearInterval(interval)
  console.log(result)
}

run().catch(error => console.error(error))

```

```javascript
// worker.js

const { workerData, parentPort, threadId } = require('worker_threads')
const { n } = workerData

const sum = async (n) => {
  console.log("Executing on thread:", threadId)
  return new Promise((resolve, reject) => {
    let sum = 0
    for (let i = 0; i < n; i++) sum += 1
    resolve(sum)
  })
}

(async () => {
  const result = await sum(n)
  parentPort.postMessage({ result, status: 'Done' })
})()

```

### Examples

* [https://github.com/PKief/nodejs-worker-threads](https://github.com/PKief/nodejs-worker-threads)

### Reading

* [https://medium.com/swlh/understanding-nodejs-worker-thread-6212b95a0928](https://medium.com/swlh/understanding-nodejs-worker-thread-6212b95a0928)
* [https://www.youtube.com/watch?v=P1sWw1bLyVg&t=4s](https://www.youtube.com/watch?v=P1sWw1bLyVg&t=4s)

