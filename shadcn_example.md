# Next.js + shadcn Example

This repository demonstrates a very small example of using **Next.js** with **shadcn/ui**.
The following steps describe how to set up the project and create a basic page.

## 1. Create a new project
```bash
npx create-next-app@latest my-shadcn-app --typescript --tailwind --src-dir --app
cd my-shadcn-app
```

## 2. Initialize shadcn/ui
```bash
npx shadcn-ui@latest init
```
This sets up the `components/ui` folder and configuration.

## 3. Replace `src/app/page.tsx`
Replace the contents of `src/app/page.tsx` with the following code:
```tsx
import { Button } from "@/components/ui/button"
import { Card, CardHeader, CardTitle, CardContent, CardFooter } from "@/components/ui/card"

export default function Home() {
  return (
    <main className="container mx-auto py-10">
      <div className="mb-6 text-center">
        <h1 className="text-3xl font-bold">Welcome to shadcn example</h1>
      </div>

      <Card className="w-full max-w-md mx-auto">
        <CardHeader>
          <CardTitle>Get Started</CardTitle>
        </CardHeader>
        <CardContent>
          <p className="text-sm text-gray-500">
            이 페이지는 shadcn/ui 컴포넌트를 사용하여 작성되었습니다.
          </p>
        </CardContent>
        <CardFooter className="flex justify-end">
          <Button>Click Me</Button>
        </CardFooter>
      </Card>
    </main>
  )
}
```

## 4. Run the development server
```bash
npm run dev
```
Open <http://localhost:3000> in your browser to see the page.
