- @Scope(BeanDefinition.SCOPE_PROTOTYPE)
- Good with mutable objects unlike singleton which is thread safe.
- The framework always creates the object instances for the prototype scope when you refer to the bean.
- Be careful with injecting a prototype-scoped bean into a singleton-scoped bean. When you do something like this, you need to be aware that the singleton instance always uses the same prototype instance, which Spring injects when it creates the singleton instance. This is usually a vicious design because the point of making a bean prototype-scoped is to get a different instance for every use.
- But injecting singleton bean into Prototype one is safe.
- How to inject prototype into singleton every time it is requested overcoming problem of singleton design?
  1- Using Object factory
  2- @Lookup
  3- retrieving manually from Application Context 