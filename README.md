# useStateWithPromise
Custom React useState hook with Promise support

# Installation

```sh
npm install --save use-state-with-promise
```

# Usage

```ts
import { useStateWithPromise } from 'use-state-with-promise';
```

```ts
const [form, setForm] = useStateWithPromise<Submission>();

<input
    type={'checkbox'}
    value={form.acceptTermsAndConditions}
    onChange={(e, value) => setForm({
        ...form,
        acceptTermsAndConditions: value
    }).then((updatedForm) => updateBackend(updatedForm))} />
```
