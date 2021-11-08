# React Typescript Notes
Changes when using Typescript with React:
- Applying types to components props
- Applying types to state in a component
- Types with event handlers
- several other assorted areas

## Types for Props
```
interface ChildProps {
  color: string;
}

export const Child = ({ color }: ChildProps) => {
  return <div>{color}</div>;
};

export const ChildAsFC: React.FC<ChildProps> = ({ color }) => {
  return <div>{color}</div>;
};
```

Using the React.FC annotation means we tell TypeScript this is a react component. Gives us access to optional React component properties (propTypes, displayName, defaultProps, contextTypes)