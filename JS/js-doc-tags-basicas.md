# JSDocs - Tags Básicas

**Autor:** Augusto TMW

### Lista de tags básicas para documentar o js com o JSDoc

* Referências:
    * http://usejsdoc.org/
    * http://speakingjs.com/es5/ch29.html

```javascript

/**
 * Basics:
 * 
 * @file File overview description
 * @author <a href="mailto:augustotmw@gmail.com">Augusto TMW</a>
 * @version 0.0.1
 * @since 0.0.1 (since which version the documented entity has been available)
 * @example
 * Contains a code example illustrating how the given entity should be used
 * @see Points to a related resource {@link MyConstructor#myMethod Works like @see, but can be used inside other tags.}
 * @see MyConstructor#myMethod
 * @see The <a href="http://example.com">Example Project</a>.
 * @requires module:example Indicates a resource that the documented entity needs. The resource description is either a namepath or a natural language description.
 * @deprecated Indicates that the entity is not supported anymore. It is a good practice to document what to use instead.
 * @description Some description of something
 * 
 * 
 * Functions/Methods:
 * 
 * @function functionName
 * @method methodName
 * @param {string} stringName string description
 * @param {number} [time=1] param with default value
 * @returns {string} Describes the return value of the function or method. Either type or description can be omitted.
 * @throws {object} Describes an exception that might be thrown during the execution of the function or method. Either type or description can be omitted.
 * @fires <className>#[event:]<eventName> Indicates that a method can fire a specified type of event when it is called
 * 
 * Variables, Parameters, and Instance Properties:
 * 
 * @name namePath variable name
 * @type {typeName} variable type
 * @member {typeName} variableName
 * @var {typeName} variableName
 * @constant variableName indicates variable's content is a constant
 * @property {boolean} flagName Document an instance property in the constructor comment
 * @default defaultValue default value of a parameter or instance property
 * 
 * 
 * Classes:
 * 
 * @constructor Marks a function as a constructor.
 * @class Marks a variable or a function as a class. In the latter case, @class is a synonym for @constructor.
 * @constructs Constructor Records that a method sets up the instance data. If such a method exists, the class is documented there.
 * @extends namePath Indicates that the documented class is the subclass of another one
 * 
 * 
 * Others:
 * 
 * @module {type} moduleName
 * 
 */

```