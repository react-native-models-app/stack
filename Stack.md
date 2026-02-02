# MODELO CRIAÇÃO REACT NATIVE STACK

Dependências obrigatorias:
```bash
npm install @react-navigation/native
npm install @react-navigation/stack
npx expo install react-native-screens react-native-safe-area-context
```

### Como montar a stack
Na raiz do projeto, crie a pasta `src/routes/stack.routes.tsx`.
```bash
import { createStackNavigator } from '@react-navigation/stack';
import HomeScreen from '@/screens/HomeScreen';
const Stack = createStackNavigator();

function StackRoutes() {
    return (
        <Stack.Navigator>
            <Stack.Screen
                name='Home'
                component={HomeScreen}
            />
        </Stack.Navigator>
    )
}
export default StackRoutes 
```
### Como chamar a stack no projeto
Na raiz do projeto, crie o arquivo `src/routes/index.tsx`.
```bash
import { NavigationContainer } from "@react-navigation/native";
import { useTheme } from "../constants/theme";
import StackRoutes from "./stack.routes";

export default function Routes() {
    const theme = useTheme();
    return (
        <NavigationContainer theme={theme}>
            <StackRoutes />
        </NavigationContainer>
    );
}
```

Documentação: 
```Bash
https://reactnavigation.org/docs/stack-navigator
```

Redes sociais: </br>
[![Instagram](https://img.shields.io/badge/Instagram-eduardocruz.dev-E4405F?logo=instagram&logoColor=white)](https://www.instagram.com/eduardocruz.dev)</br>
[![YouTube](https://img.shields.io/badge/YouTube-Tano%20Manual-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@tanomanual)</br>
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Javaverso-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/javaverso)

