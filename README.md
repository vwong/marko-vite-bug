This repo uses `@marko/vite@4.1.4` and builds fine with the command `npx marko-run build`.

Upgrade to `@marko/vite@4.1.5` or higher (up to the current 4.1.10), and notice the build failure.

The error is in [any file that uses import aliases](./src/routes/+handler.ts).
Comment out the alias import, and use the relative import instead, and it
builds fine on any version.

For reference, this feature is documented
https://vitejs.dev/config/shared-options#resolve-alias
