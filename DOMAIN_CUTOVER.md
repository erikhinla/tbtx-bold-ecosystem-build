# Domain Cutover — Fix Stale Live Sites

## Root cause

`bizbuilders.ai`, `transformby10x.ai`, and `bizbotmarketing.ai` are still attached to the **old** Vercel project `tbtx-web` (Next.js doctrine pages).

The **new static layouts** live in this repo and are already deployed to:

- https://tbtx-bold-ecosystem-build.vercel.app

They were never connected to production domains.

## Fix (5 minutes in Vercel)

### 1. Open old project and remove domains

Vercel → team **transformby10x** → project **tbtx-web** → Settings → Domains

Remove:
- `bizbuilders.ai`
- `www.bizbuilders.ai`
- `transformby10x.ai`
- `www.transformby10x.ai`
- `bizbotmarketing.ai`
- `www.bizbotmarketing.ai`

### 2. Open new project and add domains

Vercel → team **transformby10x** → project **tbtx-bold-ecosystem-build** → Settings → Domains

Add the same domains above.

### 3. Redeploy production

Deployments → Redeploy latest (after this commit lands).

### 4. Verify

- https://bizbuilders.ai should show **DIGITAL FOG IS WHEN WORK STARTS AND DOESN'T MOVE**
- https://transformby10x.ai should show **WORK IS HAPPENING / NOTHING IS MOVING**

If you still see "Infrastructure intelligence arm" or "They are lying to you" — DNS is still on `tbtx-web`.

## Preview URLs (working now)

- TBTX: https://tbtx-bold-ecosystem-build.vercel.app/transformby10x/
- BBAI: https://tbtx-bold-ecosystem-build.vercel.app/bizbuilders/
- BBM: https://tbtx-bold-ecosystem-build.vercel.app/bizbotmarketing/

## Note: ArVA cinematic site

The newer `launch/bizbuilders-ai` build (ArVA diagnostic, session API) is separate and still needs its own Vercel project (`bizbuilders-ai`) once pushed from the flow-as repo.
