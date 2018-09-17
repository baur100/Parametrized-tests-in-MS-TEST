# Parametrized-tests-in-MS-TEST

        private static IEnumerable<object[]> Inputs => new List<Foo[]>
        {
            new[] {new Foo() },
            new[] {new Foo() },
            new[] {new Foo() },
            new[] {new Foo() }
        };

        [DataTestMethod]
        [DynamicData(nameof(Inputs))]
        public async Task ConnectorOnboarding_ConnectorOnboarded_ResponseNotNull(Foo instanseOfFoo)
        {
            Assert.IsNotNull(instanseOfFoo);
        }
