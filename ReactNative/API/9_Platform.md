# select()
     ...Platform.select({
      android: {
        backgroundColor: 'green'
      },
      ios: {
        backgroundColor: 'red'
      },
      default: {
        // other platforms, web for example
        backgroundColor: 'blue'
      }
    })