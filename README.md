# Tailwind JIT Mode Errors in Next.js/Nuxt.js Build Process

This repository demonstrates a common error encountered when using Tailwind CSS in Next.js or Nuxt.js projects. The error typically arises from conflicts between Tailwind's JIT (Just-In-Time) compilation mode and the framework's build process.  The JIT compiler needs access to your template files to generate the necessary CSS; if the build process prevents this, styles may be missing or runtime errors may occur.

## Reproducing the Bug

1. Clone this repository.
2. Install dependencies: `npm install`
3. Attempt to build the project using your framework's build command (e.g., `npm run build` for Next.js).  You'll likely encounter an error indicating that Tailwind classes are not being applied or that a specific Tailwind utility is undefined.

## Solution

The solution involves carefully configuring Tailwind and your build process to ensure that the JIT compiler has the necessary access to your template files. This may require adjusting the `tailwind.config.js` file, ensuring the correct order of build steps, or modifying the framework's configuration.