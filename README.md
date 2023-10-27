# Tabla de contenidos
* [Componentes comunes](#componentescomunes)
    + [ActionsInlineComponent](#actionsinlinecomponent)
    + [ActionsListComponent](#actionslistcomponent)
    + [BannerCarouselComponent](#bannercarouselcomponent)
    + [BannerComponent](#bannercomponent)
    + [CodeEditorComponent](#codeeditorcomponent)
    + [ColorPickerComponent](#colorpickercomponent)
    + [DateTimeComponent](#datetimecomponent)
    
* [Componentes de Layouts](#componentesdelayouts)
    + [BreadcrumbsComponent](#breadcrumbscomponent)
    + [ItemMenuComponent](#itemmenucomponent)
    + [NotificationComponent](#notificationcomponent)
    + [NotificationItemComponent](#notificationitemcomponent)
    + [UserMenuComponent](#usermenucomponent)
* [Componentes de Autenticación](#componentesdeautenticación)
    + [LoginComponent](#logincomponent)
    + [LoginFormComponent](#loginformcomponent)
* [Componentes de Banners](#componentesdebanners)
    + [CreateBannerFormComponent](#createbannerformcomponent)
    + [EditBannerFormComponent](#editbannerformcomponent)
    + [ListBannersComponent](#listbannerscomponent)
* [Componentes de Multimedia](#componentesdemultimedia)
    + [CreateMediaFormComponent](#createmediaformcomponent)
    + [ListMediaComponent](#listmediacomponent)
    + [RetrieveMediaComponent](#retrievemediacomponent)
* [Componentes de Notificaciones](#componentesdenotificaciones)
    + [CreateNotificationFormComponent](#createnotificationformcomponent)
    + [ListNotificationsComponent](#listnotificationscomponent)
    + [RetrieveNotificationComponent](#retrievenotificationcomponent)
* [Componentes de Roles](#componentesderoles)
    + [CreateRoleFormComponent](#createroleformcomponent)
    + [EditRoleFormComponent](#editroleformcomponent)
    + [ListRolesComponent](#listrolescomponent)
* [Componentes de Scripts](#componentesdescripts)
    + [CreateScriptFormComponent](#createscriptformcomponent)
    + [EditScriptFormComponent](#editScriptformcomponent)
    + [ListScriptComponent](#listscriptcomponent)
    + [RetrieveScriptComponent](#retrievescriptcomponent)
* [Componentes de Usuarios](#componentesdeusuarios)
    + [CreateUserFormComponent](#createuserformcomponent)
    + [EditUserFormComponent](#edituserformcomponent)
    + [ListUserComponent](#listusercomponent)
    + [RetrieveUserComponent](#retrieveusercomponent)

# Componentes comunes <span id="ComponentesComunes"></span>

## ActionsInlineComponent <span id="ActionsInlineComponent"></span>

> Establece un componente para organizar de forma lineal las acciones a realizar en las filas de una tabla.

### Archivo:
src/components/common/table/ActionsInlineComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| row | unknown | x | Fila sobre la cual se desarrolla la acción. |
| actions | [TableActions](#tableactions) | | Acciones para realizar en la fila. |
| dense | boolean | | Estilo de forma "estrecho". |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

## ActionsListComponent <span id="ActionsListComponent"></span>

> Establece un componente para organizar en forma de lista las acciones a realizar en las filas de una tabla.
### Archivo:
src/components/common/table/ActionsListComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| row | unknown | x | Fila sobre la cual se desarrolla la acción. |
| actions | [TableActions](#tableactions) | | Acciones para realizar en la fila. |
| dense | boolean | | Estilo de forma "estrecho". |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

## BannerCarouselComponent <span id="BannerCarouselComponent"></span>

> Muestra un carrusel de imágenes o textos.

### Archivo:
src/components/common/banner/BannerCarouselComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| banners | Banner[] | x | Banners que se mostrarán en el carrusel. |
| config | BannerStyle | x | Configuración de estilos del carrusel. |
| showSpinner | boolean |  | Oculta el banner si se está mostrando un spinner. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| onLoad |  | Emite una señal de que los banners han sido cargados. |

### Slots:
Ninguno.

### Eventos:
Ninguno.

### Ver:
* [SpinnerComponent](#spinnercomponent)

## BannerComponent <span id="BannerComponent"></span>

> Lista los banners que se mostrarán en el carrusel.

### Archivo:
src/components/common/banner/BannerComponent.vue

### Props:
Ninguno.

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| onLoad | Banners[] | Emite la lista de banners. |
| onLoadError |  | Emite un error al cargar la lista de banners. |

### Slots:
Ninguno.

### Eventos:
| Nombre | Parámetros | Descripción |
| ------ | ------ | ------ |
| onLoad |  | Oculta el spinner y muestra el carrusel. |

### Ver:
* [BannerCarouselComponent](#bannercarouselcomponent)
* [SpinnerComponent](#spinnercomponent)

## CodeEditorComponent <span id="CodeEditorComponent"></span>

> Establece un editor de código personalizable.

### Archivo:
src/components/common/CodeEditorComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| modelValue | string |  | Objeto de la directiva v-model. |
| options | [EditorOptions](#editoroptions) |  | Permite cambiar el espaciado, el interlineado y la configuración de solo lectura. |
| height | string |  | Altura del editor de código. |
| width | string |  | Ancho del editor de código. |
| theme | 'vs', 'vs-dark', 'hc-black', 'hc-light' |  | Establece el tema del editor de código. |
| language | string |  | Cambia el lenguaje predeterminado del editor de código. |
| defaultLanguage | string |  | Agrega un lenguaje predeterminado al editor de código. |
| useVariables | boolean |  | Utilizar variables de auto-completado como UserSession, Response, Request, Config, Auth, entre otras. |

#### EditorOptions <span id="EditorOptions"></span>
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| lineHeight | number |  | Interlineado. |
| tabSize | number |  | Cantidad de espacios de la tabulación. |
| readOnly | boolean |  | Sólo lectura. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| update:modelValue | modelValue: any | Evento de la directiva v-model. |

### Slots:
Ninguno.

### Eventos:
Ninguno.

## ColorPickerComponent <span id="ColorPickerComponent"></span>

> Establece un selector de color.

### Archivo:
src/components/common/ColorPickerComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| modelValue | string |  | Objeto de la directiva v-model. |
| label | string |  | Etiqueta del campo de selección. |
| setButton | boolean |  | Controla si el color seleccionado se asignará al valor del campo automáticamente o si se mostrará un botón para asignar el color manualmente. |
| hasErrors | boolean |  | Controla si el campo tiene errores de validación. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| update:modelValue | modelValue: string | Evento de la directiva v-model. |

### Slots:
Ninguno.

### Eventos:
Ninguno.

## DateTimeComponent <span id="DateTimeComponent"></span>

> Establece un campo de fecha y tiempo.

### Archivo:
src/components/common/DateTimeComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| modelValue | Date o string |  | Objeto de la directiva v-model. |
| hasErrors | boolean |  | Controla si el campo tiene errores de validación. |
| title | string |  | Título. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| update:modelValue | modelValue: any | Evento de la directiva v-model. |

### Slots:
Ninguno.

### Eventos:
Ninguno.

## DetailComponent <span id="DetailComponent"></span>

> Establece un campo genérico para mostrar datos.

### Archivo:
src/components/common/DetailComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| class | ClassDetailComponent |  | Estilo predeterminado. |
| label | string | x | Etiqueta del campo. |
| value | unknown | x | Valor del campo. |
| icon | string |  | Ícono del campo. |
| isTextArea | boolean |  | Muestra el campo como un área de texto. |
| iconPosition | 'start', 'end' |  | Posición del ícono. |
| colorIcon | string |  | Color del ícono. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

## DevelopMenuComponent <span id="DevelopMenuComponent"></span>

> Contiene el menú de opciones de la aplicación en modo desarrollo (develop).

### Archivo:
src/components/common/develop/DevelopMenuComponent.vue

### Props:
Ninguno.

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

### Ver:
* [FabComponent](#fabcomponent)

## DragAndDropComponent <span id="DragAndDropComponent"></span>

> Establece una lista cuyos elementos se pueden deslizar para cambiar su orden.

### Archivo:
src/components/common/DragAndDropComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| modelValue | Date o string |  | Objeto de la directiva v-model. |
| hasErrors | boolean |  | Controla si el campo tiene errores de validación. |
| removeButtonLegend | string |  | Leyenda del botón de eliminar. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| update:modelValue | modelValue: any | Evento de la directiva v-model. |
| onRemoveElement | index: number | Emite una señal de eliminación de un elemento. |
| onUpdateElements |  | Emite una señal de actualización de la lista. |

### Slots:
Ninguno.

### Eventos:
Ninguno.

## ErrorComponent <span id="ErrorComponent"></span>

> Establece las propiedades y el estilo que tendrán los errores.

### Archivo:
src/components/common/ErrorComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| label | string | x | Nombre de etiqueta. |
| bullet | string |  | Viñetas para formatear el mensaje. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

## ErrorListComponent <span id="ErrorListComponent"></span>

> Agrupa y capta la lista de errores que derivan del servidor.

### Archivo:
src/components/common/ErrorListComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| errors | string[] |  | Lista de errores. |
| bullet | string |  | Viñetas para formatear el mensaje. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

#### Ver:
* [ErrorComponent](#errorcomponent)

## ExportDataComponent <span id="ExportDataComponent"></span>

> Muestra un modal con las opciones para exportar las filas de una tabla.

### Archivo:
src/components/common/table/ExportDataComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| exportAction(startIndex: number, limit: number) | Promise<void> | x | Acción para exportar los filas de la tabla. |
| recordsNumber | number |  | Cantidad de registros existentes de la tabla en la base de datos. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
| Nombre | Parámetros | Descripción |
| ------ | ------ | ------ |
| onTrue |  | Ejecuta la acción para exportar las filas de la tabla. |

### Ver:
* [ConfirmModalComponent](#confirmmodalcomponent)

## FabComponent <span id="FabComponent"></span>

> Botón de acción flotante que puede desplegar una o muchas acciones.

### Archivo:
src/components/common/FabComponent.vue

### Props:
_Extiende de [FabOptions](#faboptions)_
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| padding | string |  | Margen interior de los botones. |
| labelStyle | string |  | Estilo de la etiqueta de los botones. |
| verticalActionsAlign | 'left', 'center', 'right' |  | Alineación de las etiquetas cuando las acciones están ubicadas verticalmente. |
| direction | 'left', 'right', 'up', 'down' |  | Dirección de alineación de las acciones. |
| actions | [FabActions](#fabactions)[] | x | Lista de acciones. |

#### FabActions <span id="FabActions"></span>
_Extiende de [FabOptions](#faboptions)_
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| callback() | void | x | Respuesta de la acción.  |

#### FabOptions <span id="FabOptions"></span>
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| color | string |  | Color del botón. |
| icon | string |  | Ícono del botón. |
| label | string |  | Etiqueta del botón. |
| labelPosition | 'left', 'right', 'top', 'bottom' |  | Posición de la etiqueta. |
| externalLabel | boolean |  | Ubicar la etiqueta por fuera del botón. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.

## FieldComponent <span id="FieldComponent"></span>

> Conecta la lista de errores y establece el campo en el cual se mostraran los errores.

### Archivo:
src/components/common/FieldComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| errors | string[] |  | Lista de errores. |
| bullet | string |  | Viñetas para formatear el mensaje. |
| class | [ClassFieldComponent](#classfieldcomponent) |  | Clases del campo. |

#### ClassFieldComponent <span id="ClassFieldComponent"></span>
| Propiedad | Tipo | Requerido | Descripción |
| key | boolean | x | Nombre de la clase. |

### Emits:
Ninguno.

### Slots:
| Nombre | Scope | Descripción |
| ------ | ------ | ------ |
| Default | errors: string[], hasErrors: boolean | Embebe el contenido de los errores |
| Errors |  | Sobrescribe la visualización de los errores. |

### Eventos:
Ninguno.

### Ver:
* [ErrorListComponent](#errorlistcomponent)

## FileComponent <span id="FileComponent"></span>

> Establece un componente para subir archivos multimedia.

### Archivo:
src/components/common/FileComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| label | string |  | Mensaje que se mostrara en el input del archivo. |
| accept | string |  | Determina los tipos de archivos permitidos. |
| showWarningBadge | boolean |  | Muestra un mensaje de advertencia sobre el tamaño máximo permitido para subir archivos. |
| uploadButton | boolean |  | Controla si cargar el archivo con solo seleccionarlo o si mostrar un botón para cargar el archivo manualmente. |
| cancelButton | boolean |  | Muestra un botón para cancelar la operación. |

### Emits:
| Name | Parámetros | Descripción |
| ------ | ------ | ------ |
| onResponse | data: Media | Emite una señal de carga exitosa del archivo. |
| onError | error: AxiosError | Emite una señal de error. |
| onSubmit | file: File | Emite una señal de selección del archivo. |
| onCancel |  | Emite una señal de cancelación. |

### Slots:
Ninguno.

### Eventos:
| Nombre | Parámetros | Descripción |
| ------ | ------ | ------ |
| onUpload | file: File | Recibe el archivo seleccionado. |

## GaugeComponent <span id="GaugeComponent"></span>

> Establece un componente para mostrar gráficas.

### Archivo:
src/components/common/graphs/GaugeComponent.vue

### Props:
| Propiedad | Tipo | Requerido | Descripción |
| ------ | ------ | ------ | ------ |
| value | number | x | Valor de la gráfica. |
| width | number |  | Ancho de la gráfica. |
| delimiters | number[] |  | Delimitadores de la gráfica. |

### Emits:
Ninguno.

### Slots:
Ninguno.

### Eventos:
Ninguno.
