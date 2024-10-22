# Advanced InputField Component

The `InputField` component is a flexible and feature-rich input field designed for use with `react-hook-form` in TypeScript-based React applications. It extends standard form inputs with additional capabilities such as clipboard copying, password visibility toggling, input clearing, and dynamic field validation. This component is highly customizable and ideal for complex form scenarios, offering full control over input behavior and UI features.

## Key Features:
- **Dynamic Field Paths:** Supports both standard and dynamically generated field paths, making it suitable for use in deeply nested form structures.
- **Customizable Input Types:** Handles various input types such as `text`, `number`, `password`, `email`, `date`, `time`, `tel`, and `url`.
- **Clipboard Copying:** Allows users to copy input values to the clipboard with a simple button click, displaying a tooltip for feedback.
- **Password Visibility Toggle:** When used with password fields, users can toggle between showing and hiding the password.
- **Input Clearing:** Includes an option to clear the input field with a single button, which adapts based on the input type (e.g., `text` or `number`).
- **Validation Ready:** Integrates seamlessly with `react-hook-form` for field control and validation. Min and max length constraints are easily configurable.
- **Conditional Permissions:** Provides `canView` and `canEdit` properties to control whether the input field is visible and editable based on user permissions.
- **Icons for Visual Cues:** Supports additional visual cues like verification checks (using `CheckCircleIcon`) and cancel actions (using `CancelIcon`) through Material-UI icons.
- **Custom Event Handlers:** Allows for the use of custom `onChange` handlers to perform additional actions when the input value changes.

## Props:
- `name`: The dynamic field path managed by `react-hook-form`.
- `control`: Form control provided by `react-hook-form`.
- `label`: The label displayed for the input field.
- `type`: Specifies the type of the input (e.g., `text`, `number`, `password`).
- `placeholder`: Optional placeholder text for the input.
- `clipboard`: Enables a clipboard icon for copying the input value.
- `verify`: Displays a verification icon to indicate successful verification.
- `showPasswordToggle`: Toggles the visibility of password input fields.
- `clearInput`: Provides a clear button to reset the field value.
- `required`: Marks the field as required.
- `canView`: Controls whether the input field is visible.
- `canEdit`: Controls whether the input field is editable.
- `minLength`, `maxLength`: Defines the minimum and maximum length for the input value.
- `onChange`: Optional custom handler for input value changes.

## Example Usage:
```tsx
<InputField
    name="email"
    label="Email Address"
    type="email"
    control={control}
    placeholder="Enter your email"
    required
    clipboard
    verify
    canEdit={userCanEdit}
    canView={userCanView}
/>
