# As a Node.js Developer

I'm not a huge fan of [JavaScript](https://www.javascript.com) as a language but I've found [Node.js](https://nodejs.org/en/) to be a very productive and robust framework for building web services. This is in large part due to [npm](https://www.npmjs.com) and the massive collection of available packages.

I tend to use [Express](https://expressjs.com) if I am starting a new web service. Both [Angular](https://angular.io) ([MEAN](http://mean.io)) and [React](https://reactjs.org) play well with Node.js web services running with Express.

I use [bunyan](https://www.npmjs.com/package/bunyan) for logging and use [bunyan-cloudwatch](https://www.npmjs.com/package/bunyan-cloudwatch) when running in AWS to log events to [CloudWatch](https://aws.amazon.com/cloudwatch/) directly. I use the [AWS SDK for Node.js](https://aws.amazon.com/sdk-for-node-js/) to connect to various AWS services like [SQS](https://aws.amazon.com/sqs/). All of my Node.js web services or microservices use [MySQL](https://www.mysql.com) as a backend database.

I use web sockets heavily for facilitating real-time data synchronization. [socket.io](https://www.npmjs.com/package/socket.io) has worked well for this in Node.js. To ensure messages are broadcast to clients across all instances, [socket.io-redis](https://www.npmjs.com/package/socket.io-redis) is used.

I write all of my JavaScript code using [WebStorm](https://www.jetbrains.com/webstorm/), also by Jetbrains. I write my JavaScript with [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) enabled and use [eslint](https://eslint.org) to automatically clean up my code.

As with iOS code, I write a lot of unit and integration tests for my Node.js web services. I use a combination of [mocha](https://mochajs.org) and [chai](http://chaijs.com) for writing tests and [istanbul](https://istanbul.js.org) for code coverage. Again, this gives me the ability to safely update package dependencies more aggressively than would otherwise be possible.

In addition to normal web services, I also use Node.js to write microservices which run in [AWS Lambda](https://aws.amazon.com/lambda/) and are fronted by [API Gateway](https://aws.amazon.com/api-gateway/). If I can, I use [Swagger](https://swagger.io) to document the API and to autogenerate the endpoints.

I used to use [SendWithUs](https://www.sendwithus.com/index) to create email templates, merge them, and send them out using [SendGrid](https://sendgrid.com). I've since replaced all of the SendWithUs functionality with SQS and Lambda. SendGrid's [Event Webhook](https://sendgrid.com/docs/API_Reference/Webhooks/event.html) sends email-related events back to the web service so their events can be aggregated with other application and service events.

I've used a similar architecture to deliver several [Alexa](https://developer.amazon.com/alexa) skills.