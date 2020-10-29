## Documentation

This is a fork of:
>https://github.com/abelheinsbroek/chartjs-plugin-crosshair

with these additional features:

- Ability to show an horizontal line in addition to the vertical one
- Ability to selectively chose wether to show vertical, horizontal or both tracelines
- Ability to disable traceline even if plugin is loaded

## Notes and warings
 
 - Unlike original implementation, note that all options (line tracing, zoom, sync) are DISABLED by default. You need to explicitly enable them in the crosshair settings object (see below)

## Configuration example
This example shows the additional options compared to the original implementation. For the standard option, check out the original readme

```javascript
new Chart(ctx, {
  // ... data ...
  options: {
    // ... other options ...
    tooltips: {
      mode: 'interpolate',
      intersect: false
    },
    plugins: {
      crosshair: {
        line: {
          enabled: true, //globally enables or disables line tracing
          drahHorizontal: true, //selectively enable/disable horizontal traceline
          drawVertical: true //selectively enable/disable vertical traceline
          //...
        },
        sync: {
          //...
        },
        zoom: {
          //..
        },
        callbacks: {
          //..
        }
      }
    }
  }
});
```