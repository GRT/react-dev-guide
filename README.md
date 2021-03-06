# react-dev-guide
GRT React style guide

## Examples to steal from
 - [airbnb](https://github.com/airbnb/javascript/tree/master/react)
 - [David Chang](http://reactjsnews.com/react-style-guide-patterns-i-like/)
 - [React 2016 Best Practices](https://blog.risingstack.com/react-js-best-practices-for-2016/)


## Goals
The purpose of this repo is to standardize on one set of best practices, tips and tricks for React development at GRT and to provide a reference for new React devs. This will allow those of us that are new to React to get up to speed quickly and those of us with some experience to move easily between projects and find our way around familiar codebases.

## Submitting Issues
If you see something say something. The best way to report a bug, request a feature or just start a conversation is to create and issue on the relevant repository. For example if you're infuriated by the grammar of this document, you're encouraged to [create and issue here](https://github.com/GRT/react-dev-guide/issues).  [More on Github issues](https://guides.github.com/features/issues/).

## Contributing
There are 2 types of contributors on our projects.
### Team Members
If you're assigned to a project team for a given product, you should always create a feature branch off of master and do your work there.  Once you're done and/or ready for a second set of eyes, please push your feature branch and [create a pull request](https://help.github.com/articles/creating-a-pull-request/).  This pull request will be were we collaborate in code review and once at least one other team memeber has given and LGTM :+1:.  You can merge to master and delete your feature branch.
### Outside Contributors
Non team members should also be encouraged to contribute. In this case devs should [fork the target repo](https://help.github.com/articles/fork-a-repo/) implement their changes in that fork and [create a pull request](https://help.github.com/articles/using-pull-requests/) against the source project. Team members will review, discuss, collaborate on the PR before merging.

## Pull Requests
Pull requests should be as detailed as possible in describing the changes and reasoning behind them. It's advisable to create PRs early to allow feedback and participation from others in the team. If you'd like to create a PR that's not yet ready to be mearges, you can use the text **[WIP]** in the title. To indicate that you'd like some feedback include **[Review]** in the title.

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

## Props
Proptypes should be defined in you component
Example:

```
 ClassName.propTypes = { mode: React.PropTypes.string };
```
## TBD
 - Installation
 - Running the code
 - [Testing](https://github.com/GRT/onesie/issues/9)
 - npm run tasks
 - Extend Versus Create
 - Nested Components
 - Size
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

## [Project Structure] (http://reactjsnews.com/structuring-react-projects/) | *Work in Progress*
###### File Naming
Starting the component names (i.e., App.jsx) with an uppercase letter makes them easy to discover. 

###### Component Index.js
Use an index.js file to export the component this provides us with a neat entry points to the files so they are easy to consume from elsewhere.Each component is a self-contained entity now. We can use for example CSS Modules to underline this point. Extracting these components from the project would be easy now given how self-contained they are.

```
//src/ClusterThumbView/index.js
import ClusterThumbView from './ClusterThumbView.jsx';
export default ClusterThumbView
```

###### Tests
The tests related to each component are trivial to find now. We still might want to have a /tests directory at the project root in order to deal with higher level tests.

```
src $ tree
.
├── components
│   ├── Note
│   │   ├── Note.jsx
│   │   ├── index.js
│   │   ├── note.css
│   │   └── note_test.jsx
│   ├── Routes
│   │   ├── Routes.jsx
│   │   ├── index.js
│   │   └── routes_test.jsx
│   └── index.js
├── index.jsx
├── main.css
└── views
    ├── Home
    │   ├── Home.jsx
    │   ├── home.css
    │   ├── home_test.jsx
    │   └── index.js
    ├── Register
    │   ├── Register.jsx
    │   ├── index.js
    │   ├── register.css
    │   └── register_test.jsx
    └── index.js
```

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
