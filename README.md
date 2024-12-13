# Accessing props or state before component mount in React Native

This repository demonstrates a common error in React Native: attempting to access component props or state before the component has finished mounting.  The `bug.js` file shows the problematic code, while `bugSolution.js` presents the corrected version.

## Problem

Accessing `this.props` or `this.state` within the constructor or before `componentDidMount` can lead to `undefined` values, resulting in unexpected behavior or crashes. This is because the component's props and state are not fully initialized until after the mounting process is complete.

## Solution

The solution is to ensure you only access `this.props` and `this.state` after the component has mounted.  The ideal place to perform any actions that depend on these values is within the `componentDidMount` lifecycle method.