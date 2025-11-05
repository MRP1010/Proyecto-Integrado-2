# Proyecto-Integrado-2
Al operador de telecomunicaciones Interconnect le gustaría poder pronosticar su tasa de cancelación de clientes. Si se descubre que un usuario o usuaria planea irse, se le ofrecerán códigos promocionales y opciones de planes especiales. El equipo de marketing de Interconnect ha recopilado algunos de los datos personales de sus clientes.

### Servicios de Interconnect

Interconnect proporciona principalmente dos tipos de servicios:

1. Comunicación por teléfono fijo. El teléfono se puede conectar a varias líneas de manera simultánea.
2. Internet. La red se puede configurar a través de una línea telefónica (DSL, *línea de abonado digital*) o a través de un cable de fibra óptica.

Algunos otros servicios que ofrece la empresa incluyen:

- Seguridad en Internet: software antivirus (*ProtecciónDeDispositivo*) y un bloqueador de sitios web maliciosos (*SeguridadEnLínea*).
- Una línea de soporte técnico (*SoporteTécnico*).
- Almacenamiento de archivos en la nube y backup de datos (*BackupOnline*).
- Streaming de TV (*StreamingTV*) y directorio de películas (*StreamingPelículas*)

La clientela puede elegir entre un pago mensual o firmar un contrato de 1 o 2 años. Puede utilizar varios métodos de pago y recibir una factura electrónica después de una transacción.

### Pasos Claves

Ingeniería de Características de Tiempo: La creación de la variable duration_days / duration_months fue la acción de mayor valor predictivo, clave para que los modelos de boosting alcanzaran un alto rendimiento.

Uso de Métricas Correctas: Enfocarse en ROC AUC y APS para medir el rendimiento, en lugar de solo Accuracy, fue crucial debido al desbalance de clases.

El proceso iterativo de usar Grid Search y ajustar los parámetros (max_depth, min_samples_leaf) permitió transformar un modelo con sobreajuste (Decision Tree) en un modelo estable y de alto rendimiento.

Selección del Modelo de Ensamble Avanzado: La elección final del CatBoost demostró ser la mejor, ya que superó a todos los demás modelos en la métrica clave de prueba.

### Conclusiones

El analisis EDA ha revelado que la duración del contrato, el tipo de contrato, el método de pago, la presencia de servicios adicionales y el perfil demográfico del cliente (ciudadano mayor, parther, dependencia) son factores clave relacionados con la cancelación.

Los hallazgos de este análisis proporcionan información valiosa para el equipo de marketing. Las estrategias de retención deben enfocarse en:

Clientes con contratos mes a mes.

Clientes que utilizan cheque electrónico como método de pago.

Clientes que no tienen servicios adicionales; se podría incentivar la contratación de estos servicios.

Clientes que son personas mayores o que no son parther, ni tenen una dependencia, ofreciéndoles planes o promociones específicas.

Clientes nuevos o con poca antigüedad, ya que el riesgo de cancelación es mayor en las primeras etapas del contrato pr o que deberian incremenar los beneficios en los contraros de mayor tiempo.

Hemos desarrollado un modelo predictivo robusto utilizando CatBoost que puede ayudar a identificar a los clientes con mayor riesgo de cancelación. La información sobre las características más importantes proporciona una base sólida para que el equipo de marketing diseñe e implemente estrategias de retención dirigidas y efectivas en estos sectores.
