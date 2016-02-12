# react-dev-guide
GRT React style guide

## Examples to steal from
 - [airbnb](https://github.com/airbnb/javascript/tree/master/react)
 - [David Chang](http://reactjsnews.com/react-style-guide-patterns-i-like/)

## Goals
The purpose of this repo is to standardize on one set of best practices, tips and tricks for React development at GRT and to provide a reference for new React devs. This will allow those of us that are new to React to get up to speed quickly and those of us with some experience to move easily between projects and find our way around familiar codebases.

## Submitting Issues
If you see something say something. The best way to report a bug, request a feature or just start a conversation is to create and issue on the relevant repository. For example if you're infuriated by the grammar of this document, you're encouraged to [create and issue here](https://github.com/GRT/react-dev-guide/issues).  [More on Github issues](https://guides.github.com/features/issues/).

## Contributing
There are 2 types of contributors on our projects.
### Team Members
If you're assigned to a project team for a given product, you should always create a feature branch off of master and do your work there.  Once you're done and/or ready for a second set of eyes, please push your feature branch and [create a pull request](https://help.github.com/articles/creating-a-pull-request/).  This pull request will be were we collaborate in code review and once at least one other team memeber has given and LGTM :+1:.  You can merge to master and delete your feature branch.
### Outside Contributors



## Code Reviews

## React Class Syntax
We prefer to define classes using the [JS ES6 Class Syntax](https://facebook.github.io/react/docs/reusable-components.html#es6-classes)

```
class HelloMessage extends React.Component {
  render() {
    return <div>Hello {this.props.name}</div>;
  }
}
ReactDOM.render(<HelloMessage name="Sebastian" />, mountNode);
```

## Mixins
ES6 classes do not support mixins and neither do we. [Dan Abramov on mixins in React](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750#.ecm9uuewt)

## TBD
 - Installation
 - Running the code
 - [Testing](https://github.com/GRT/onesie/issues/9)
 - npm run tasks
 - Extend Versus Create
 - Nested Components
 - Size
 - Props and State
 - Managing The State
 - Events
 - Design Patterns
 - PR Process
 - Before You PR!
 - Submitting a PR
 - Assign your PRs
 - Conventions
 - Version Bumping and Publishing
 - Bad Practices
 - Additional dependencies
 - jQuery and Underscore
 - Five Lines
 - File Naming

## Method Organizations
We lay out the methods of a component in life-cycle order:

class Foo extends React.Component({
  displayName : ''
  propTypes: {}
  statics: {}
  getDefaultProps() {},
  getInitialState() {},
  componentWillMount() {},
  componentDidMount() {},
  componentWillReceiveProps() {},
  shouldComponentUpdate() {},
  componentWillUpdate() {},
  componentDidUpdate() {},
  componentWillUnmount() {},
  _getFoo() {},
  _fooHelper() {},
  _onClick() {},
  render() {}
});


 - displayName
 - Conditional HTML
 - JSX as a Variable or Return Value
 - Self-Closing Tags
 - List Iterations
 - Formatting Attributes
 - Sub-components
 - Bit-Wise Operators
 - ES6
 - Basic Rules
Class vs React.createClass vs stateless
Naming
Declaration
Alignment
Quotes
Spacing
Props
Parentheses
Tags
Methods
Ordering
isMounted
