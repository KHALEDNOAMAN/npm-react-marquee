# React Marquee - Advanced Examples

## Basic Usage
```tsx
import { Marquee } from "react-marquee";

function App() {
  return (
    <Marquee speed={50} direction="left">
      <span>Your scrolling content here</span>
    </Marquee>
  );
}
```

## Pause on Hover
```tsx
<Marquee pauseOnHover gradient={false}>
  {logos.map(logo => <img key={logo.id} src={logo.url} />)}
</Marquee>
```

## Performance Tips
| Tip | Why |
|-----|-----|
| Use Web Animations API | GPU-accelerated, no JS frame loop |
| Limit children count | Fewer DOM nodes = smoother scroll |
| Avoid heavy images | Compress and lazy-load assets |
| Set will-change | Hint browser for compositing |

## vs Other Libraries
| Feature | react-marquee | react-fast-marquee |
|---------|-------------|-------------------|
| Dependencies | Zero | 0 |
| Animation | Web Animations API | CSS |
| Bundle size | ~2KB | ~4KB |
| Tree-shakable | Yes | Partial |