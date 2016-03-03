# Protractor-Config-Simple

### config-simple.js
```bash
exports.config = {
  seleniumAddress: 'http://localhost:4444/wd/hub',

  capabilities: {
    'browserName': 'chrome'
  },

  specs: ['jasmine-angularOrg-spec.js'],

  jasmineNodeOpts: {
    showColors: true
  }
};
```

### jasmine-angularOrg-spec.js
```bash
// example-spec.js
describe('angularjs homepage', function() {
  it('should greet the named user', function() {
    browser.get('http://www.angularjs.org');

    element(by.model('yourName')).sendKeys('Julie');

    var greeting = element(by.binding('yourName'));

    expect(greeting.getText()).toEqual('Hello Julie!');
  });
});
```

## usage
```bash
# If neededed
  webdriver-manager update 
  
  webdriver-manager start
  
  protractor ./config-simple.js
```
