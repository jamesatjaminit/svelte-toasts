# Docs

## Store

- [`ToastStore`](#ToastStore)

## Components

- [`BootstrapToast`](#bootstraptoast)
- [`FlatToast`](#flattoast)
- [`ToastContainer`](#toastcontainer)

---

## `ToastStore`

```javascript
import { toasts } from 'svelte-toasts';
```

Store `toasts` contains an array of toasts objects. It has following methods:

<table class="min-w-full divide-y divide-gray-200"><thead class="bg-gray-100"><tr><th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase">Name </th><th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase">Type </th><th scope="col" class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase">Description </th></tr></thead> <tbody class="bg-white divide-y divide-gray-200"><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">add</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">This is key function to show toast. You can pass options and modify the generated toast.</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">removeAll</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">This function removes all toasts and clears store state to empty array</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">removeLast</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">This function removes one toast (if any) that was generated at the end</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">getById</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">This function returns toast data for given id. Every toast has a unique uid</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">setDefaults</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">This function sets default options so you don't need to pass those options again and again, e.g. theme, placement etc.</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">success</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Show success/green toast.</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">info</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Show info/blue toast.</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">error</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Show error/red toast.</div></td> </tr><tr><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 text-bold">warn</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Function</div></td><td class="px-6 py-4" style=""><div class="text-sm text-gray-600 undefined">Show warn/orange toast.</div></td> </tr></tbody></table>

## `BootstrapToast`

```javascript
import { BootstrapToast } from 'svelte-toasts';
```

### Props

| Prop name | Kind             | Reactive | Type                                    | Default value        | Description                  |
| :-------- | :--------------- | :------- | :-------------------------------------- | -------------------- | ---------------------------- |
| theme     | <code>let</code> | No       | <code> [Theme](#theme)</code>           | <code>'light'</code> | Default theme for all toasts |
| data      | <code>let</code> | No       | <code> [ToastProps](#ToastProps)</code> | <code>{}</code>      | Default theme for all toasts |

### Slots

| Slot name  | Default | Props | Fallback                                                                                                                                                                                                                                                                                                                                                                   |
| :--------- | :------ | :---- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| close-icon | No      | --    | <code>&lt;svg<br /> xmlns="http://www.w3.org/2000/svg"<br /> class="bx--toast-notification\_\_close-icon"<br /> width="20"<br /> height="20"<br /> viewBox="0 0 32 32"<br /> aria-hidden="true"<br /> &gt;<br /> &lt;path<br /> d="M24 9.4L22.6 8 16 14.6 9.4 8 8 9.4 14.6 16 8 22.6 9.4 24 16 17.4 22.6 24 24 22.6 17.4 16 24 9.4z"<br /> /&gt;<br /> &lt;/svg&gt;</code> |
| extra      | No      | --    | --                                                                                                                                                                                                                                                                                                                                                                         |
| icon       | No      | --    | <code>Svg icons based on type<code>                                                                                                                                                                                                                                                                                                                                        |

### Events

None.

## `FlatToast`

```javascript
import { FlatToast } from 'svelte-toasts';
```

### Props

| Prop name | Kind             | Reactive | Type                                     | Default value        | Description                  |
| :-------- | :--------------- | :------- | :--------------------------------------- | -------------------- | ---------------------------- |
| theme     | <code>let</code> | No       | <code> [Theme](#theme) </code>           | <code>'light'</code> | Default theme for all toasts |
| data      | <code>let</code> | No       | <code> [ToastProps](#ToastProps) </code> | <code>{}</code>      | Default theme for all toasts |

### Slots

| Slot name  | Default | Props | Fallback                                                                                                                                                                                                                                                                                                                                                                   |
| :--------- | :------ | :---- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| close-icon | No      | --    | <code>&lt;svg<br /> xmlns="http://www.w3.org/2000/svg"<br /> class="bx--toast-notification\_\_close-icon"<br /> width="20"<br /> height="20"<br /> viewBox="0 0 32 32"<br /> aria-hidden="true"<br /> &gt;<br /> &lt;path<br /> d="M24 9.4L22.6 8 16 14.6 9.4 8 8 9.4 14.6 16 8 22.6 9.4 24 16 17.4 22.6 24 24 22.6 17.4 16 24 9.4z"<br /> /&gt;<br /> &lt;/svg&gt;</code> |
| extra      | No      | --    | --                                                                                                                                                                                                                                                                                                                                                                         |
| icon       | No      | --    | <code>Svg icons based on type<code>                                                                                                                                                                                                                                                                                                                                        |

### Events

None.

## `ToastContainer`

```javascript
import { ToastContainer } from 'svelte-toasts';
```

### Props

| Prop name    | Kind             | Reactive | Type                                   | Default value               | Description                                                            |
| :----------- | :--------------- | :------- | :------------------------------------- | --------------------------- | ---------------------------------------------------------------------- |
| theme        | <code>let</code> | No       | <code> [Theme](#Theme) </code>         | <code>'dark'</code>         | Default theme for all toasts                                           |
| placement    | <code>let</code> | No       | <code> [Placement](#Placement) </code> | <code>'bottom-right'</code> | Default placement for all toasts                                       |
| type         | <code>let</code> | No       | <code> [ToastType](#ToastType) </code> | <code>'info'</code>         | Default type of all toasts                                             |
| showProgress | <code>let</code> | No       | <code> boolean </code>                 | <code>false</code>          | Show progress if showProgress is true and duration is greater then 0   |
| duration     | <code>let</code> | No       | <code> number </code>                  | <code>3000</code>           | Default duration for all toasts to auto close. 0 to disable auto close |
| width        | <code>let</code> | No       | <code> 'string' </code>                | <code>'320px'</code>        | Width of all toasts                                                    |

### Slots

| Slot name | Default | Props                                             | Fallback |
| :-------- | :------ | :------------------------------------------------ | :------- |
| --        | Yes     | <code>{ data: [ToastProps](#ToastProps) } </code> | --       |

### Events

None.

## Types

#### `Theme`

```ts
export type Theme = 'dark' | 'light';
```

#### `ToastType`

```ts
export type ToastType = 'success' | 'info' | 'error' | 'warn';
```

#### `Placement`

```ts
export type Placement =
  | 'bottom-right'
  | 'bottom-left'
  | 'top-right'
  | 'top-left'
  | 'top-center'
  | 'bottom-center'
  | 'center-center';
```

#### `ToastProps`

```ts
export interface ToastProps {
  uid: number;
  title?: string;
  description: string;
  duration: number;
  type: ToastType;
  theme?: Theme;
  placement: Placement;
  showProgress?: boolean;
  remove?: Function;
  update?: Function;
  onRemove?: Function;
  onClick?: Function;
}
```

#### `ToastStore`

```ts
export interface ToastStore extends Writable<ToastProps[]> {
  add(options: Partial<ToastProps>): ToastProps;
  success(options: Partial<ToastProps>): ToastProps;
  success(description: string): ToastProps;
  success(description: string, options: Partial<ToastProps>): ToastProps;
  success(
    title: string,
    description: string,
    options?: Partial<ToastProps>
  ): ToastProps;

  info(options: Partial<ToastProps>): ToastProps;
  info(description: string): ToastProps;
  info(description: string, options: Partial<ToastProps>): ToastProps;
  info(
    title: string,
    description: string,
    options?: Partial<ToastProps>
  ): ToastProps;

  error(options: Partial<ToastProps>): ToastProps;
  error(description: string): ToastProps;
  error(description: string, options: Partial<ToastProps>): ToastProps;
  error(
    title: string,
    description: string,
    options?: Partial<ToastProps>
  ): ToastProps;

  warn(options: Partial<ToastProps>): ToastProps;
  warn(description: string): ToastProps;
  warn(description: string, options: Partial<ToastProps>): ToastProps;
  warn(
    title: string,
    description: string,
    options?: Partial<ToastProps>
  ): ToastProps;

  getById(uid: number): ToastProps;
  clearAll(): void;
  clearLast(): void;
  setDefaults(options: Partial<ToastProps>): void;
}
```
