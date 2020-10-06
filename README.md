# Performance Testing Class


## Front End

### Lighthouse



#### Installation

```sh
npm i -g lighthouse
```

#### Running Tests

```sh
lighthouse --view https://starwest.techwell.com/

lighthouse --budgetPath ./budget.json --view https://starwest.techwell.com/

lighthouse --budgetPath ./budget.strict.json --view https://starwest.techwell.com/

lighthouse --budgetPath ./budget.easy.json --view https://starwest.techwell.com/
```

## Back End

### Artillery

#### Installation

```sh
npm install -g artillery@latest

npm install -g artillery-plugin-expect
```

#### Running Tests

```sh
artillery run test-00-basic-get.yaml -o report.yml
artillery run test-01-simple-post.yaml -o report.yml
artillery run test-02-corr-param.yaml -o report.yml

artillery report report.yml
```

##### Sample App
```sh
docker run -d -p 8080:8080 kaushald/leakyserver:0.1.0
```