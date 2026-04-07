
# Prequisites

1. Install Node LTS version (LTS v24.14.1 (Krypton) or later LTS)

```
C:\Program Files\nodejs\
Install "Tools for Native Modules" (uncheck during install)
```

2. Install Angular CLI

```
npm install -g @angular/cli
ng version
```

3. Create Angular App project with name "nautilus-hub-web"

- opcja style scs: Sassy CSS, odpowiednia do PrimeNG
- opcja ssr: server side rendering (prerenderowanie HTML po stronie serwera)

```
ng new nautilus-hub-web --style=scss --routing --ssr=false
# No anonymous usage 
# Claude
```

4. Install PrimeNG framework in the project root directory

```
cd nautilus-hub-web
npm install primeng @primeuix/themes
```

- add the primeng import in the project file "app.config.ts" (Aura,Material,Lara,Nora)

```
[\] import { ApplicationConfig, provideBrowserGlobalErrorListeners } from '@angular/core';
[\] import { provideRouter } from '@angular/router';
[+] import { provideHttpClient } from '@angular/common/http';[

[+] import { providePrimeNG } from 'primeng/config';
[+] import Lara from '@primeuix/themes/lara';

[\] import { routes } from './app.routes';

[\] export const appConfig: ApplicationConfig = {
[\]  providers: [
[\]    provideBrowserGlobalErrorListeners(),
[\]    provideRouter(routes),
[+]    provideHttpClient(),
[+]    providePrimeNG({
[+]            theme: {
[+]                preset: Lara
[+]            }
[+]        })
[\] ]
[\] };
```

5. Launching an angular project
- in the project root directory

```
ng serve
```