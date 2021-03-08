# mailazy-node

> Mailazy NodeJs SDK Client


## Table of Contents

* [Install](#install)
* [Usage](#usage)
* [License](#license)


## Install

[npm][]:

```sh
npm install mailazy-node
```

[yarn][]:

```sh
yarn add mailazy-node
```


## Usage

```js
const MailazyClient = require('mailazy-node');

const client = new MailazyClient({ accessKey: '', accessSecret: '' });

const fn = async () => {
    try {
        const resp = await client.send({
            to: 'test@example.com', // required
            from: 'no-reply@example.com', // Use domain you verified, required
            subject: '', // required
            text: '',
            html: '',
        });
        console.log("resp: " + resp);
    } catch (e) {
        console.log("errror: " + e);
    }
}

fn();
```

## License

[MIT](LICENSE) © Mailazy


##

[npm]: https://www.npmjs.com/

[yarn]: https://yarnpkg.com/
