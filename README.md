# Verso

A logical markup language born from another universe to bridge the gap between markup and programming languages.

## What is Verso?

Verso is a logical markup language designed to seamlessly integrate HTML structure with JavaScript functionality in a single, coherent syntax. It emerged from the need to maintain clean separation of concerns while reducing the complexity of managing multiple languages in web development.

## Why Verso?

Traditional web development often requires juggling between HTML markup and JavaScript logic, leading to scattered code and maintenance challenges. Verso solves this by:

- Providing a unified syntax that feels natural for both markup and logic
- Eliminating the need to switch between different file types and syntaxes
- Offering a backend-agnostic approach to component processing
- Maintaining simplicity while supporting complex programming patterns

## Key Features

- **Backend Agnostic**: Can be processed by any backend language, no Node.js required
- **Familiar Syntax**: Combines HTML-like markup with JavaScript-like logic
- **Component-Based**: Built with component-driven development in mind
- **Logical Markup**: Seamlessly integrate programming logic within markup
- **Simple Yet Powerful**: Easy to learn but capable of handling complex scenarios

## Example

```xml
    <components basedir='components'>

        <import file='slider/slider.twig' />
        <import file='btns/btn-primary.twig' />

        <let name='data' value='hi' />
        <let name='list' value='[1,2,3]' />

        <let name='cb' value='function(prop = {}) { return 1; }' />

        <function async name='processData' params='name = luis, age = 25'>
            const result = await fetchUserData(name);
            
            return {
                ...result,
                age,
                processed: true
            }
        </function> 

        <function name='handleClick' params='event'>
            console.log('Clicked!', event.target);
        </function>   

        <!-- Listener explícito para eventos -->
        <listen on='button' event='click' handler='handleClick' />
        
        <!-- Multiple listeners -->
        <listen on='#myForm'>
            <event name='submit' handler='handleSubmit' />
            <event name='reset' handler='handleReset' />
        </listen>                   

        <let name='obj'>
            nombre: 'Juan',
            edad: 25,
            saludar: () => console.log('Hola!')            
        </let>

        <foreach var='num' in='list'>

        </foreach>
            
        <slide imgs='[ 1, 2, 3, 4 ]' />
            
        <button text='Click here' />

    </components>
```

## Philosophy

Verso was created with the belief that developers shouldn't have to constantly switch contexts between markup and logic. It provides a unified way to express both structural and behavioral aspects of web components, while remaining simple enough to be processed by any backend language.

## Getting Started

[Documentation and implementation guides coming soon]

## Benefits

- 🎯 Single source of truth for component structure and logic
- 🔄 Seamless integration of markup and programming concepts
- 🛠 Backend language agnostic
- 📦 Component-based architecture support
- 🌐 Universal processing capability
- 🧩 Clean and intuitive syntax

## License

MIT License
