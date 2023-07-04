# Uniendo nuestra API y Front-End 😎 !

En este desafiante proceso de vincular nuestra **API** con el **front-end**, es fundamental tener paciencia y recordar que cada uno de nosotros puede tener construido su **front-end de manera diferente**. Por lo tanto, necesitaremos un poco más de tiempo y es posible que tengamos que realizar algunos **console.log()** adicionales 😅. 

****Sin embargo, con determinación y trabajo en equipo, lograremos alcanzar nuestro objetivo!****

---
# Pasos a seguir

 - [ ] 1. Creo el .env y agregar a .gitignore
 
		VITE_REACT_APP_URL=http://localhost:8080/api/v1
---
 
 - [ ] 2. Creo el .evn.example
 
		VITE_REACT_APP_URL=http://localhost:8080/api/v1
---
 - [ ] 3. Ir a: `src/components/home/Filtercategory.jsx` (dos url para
       actualizar)

	- Importo: 
						
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL
						
		- [ ] a) Reemplazo la variable url por : 
				
				const url = `${URL_BASE}/categories`
				
		- [ ] b) Reemplazo la variable url por : 
				
				const url = `${URL_BASE}/products?categoryId=${id}`
---       
 - [ ] 4. Ir a: `src/components/ProductId/SimilarProduct.jsx` (una url para
       actualizar)

	- Importo: 
						
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL
						
		- [ ] a) Reemplazo la variable url por : 
				
				const url = `${URL_BASE}/products?categoryId=${product?.categoryId}`
---
- [ ] 5. Ir a: `src/hooks/useAuthentication.js` (dos url para
       actualizar)
							
	- [ ] a)  
		
				const URL_BASE = import.meta.env.VITE_REACT_APP_URL
				
				const url = `${URL_BASE}/users`

	- [ ] b) 
				
				const URL_BASE = import.meta.env.VITE_REACT_APP_URL
				
				const url = `${URL_BASE}/users/login`
---
- [ ] 6. Ir a: `src/hooks/useCrudCart.js` (tres url para
       actualizar)
							
	- [ ] a)  addProductToCar
		
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL

			const url = `${URL_BASE}/cart`

	- [ ] b)  deleteProductFromCart
				
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL

			const url = `${URL_BASE}/cart/${id}`

	- [ ] c)  updateProductFromCard
				
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL

			const url = `${URL_BASE}/cart/${id}`
---
- [ ] 7. Ir a: `src/hooks/usePurcharses.js` (una url para
       actualizar)
							
	- [ ] a)  
		
				const URL_BASE = import.meta.env.VITE_REACT_APP_URL
				
				const url = `${URL_BASE}/purchase`
---
- [ ] 8. Ir a: `src/pages/productId.jsx` (una url para
       actualizar)
							
	- [ ] a)  
		
				const URL_BASE = import.meta.env.VITE_REACT_APP_URL
				
				const url = `${URL_BASE}/products/${id}`
---
- [ ] 9. Ir a: `src/store/slices/cart-slice.js` (una url para
       actualizar)
							
	- [ ] a)  
		
				const URL_BASE = import.meta.env.VITE_REACT_APP_URL
				
				const url = `${URL_BASE}/cart`
---
- [ ] 10. Ir a: `src/store/slices/products-slice.js` (una url para
       actualizar)
							
	- [ ] a)  
		
			const URL_BASE = import.meta.env.VITE_REACT_APP_URL

			export const getAllProductsThunk = (url = `${URL_BASE}/products`) => dispatch => {
				axios.get(url)
				.then(res => dispatch(setProductsGlobal(res.data)))
				.catch(err => console.log(err))
			}
---
- [ ] 11. Ir a: `src/components/home/CardProduct.jsx` (modificar images)
							
	- [ ] a)  

				<img  className='header__img image1'  src={product?.productImgs[0].url}  alt={product.title}  />

				<img  className='header__img image2'  src={product?.productImgs[1].url}  alt={product.title}  />

---
- [x] 12. Ir a: `src/components/productId/SliderImgs.jsx`
							
	- [ ] a)  
	
			 product?.productImgs.map
---
- [ ] 13. Ir a: `src/components/cart/ProductInCart.jsx`
							
	- [ ] a)  
	
			 <img  className='prodcart__img'  src={prodCart?.product?.productImgs[0]?.url}  alt={prodCart?.product.title}  />
---
- [ ] 14. Ir a: `src/components/Purcharses/ProductInCart.jsx`
							
	- [ ] a)  
	
			<img  className='productPurchase__img'  src={prodPurchased.product?.productImgs[0].url}  alt=""  />
 
 
	
# TAREA MORAL 😅

**Elaborar un archivo README para presentar el front-end como el backend.**

1.  **Título claro:** Proporciona un título descriptivo y conciso que indique claramente los propósitos de los proyectos.
    
2.  **Descripción general:** Brinda una breve descripción de los proyectos, sus propósitos y su funcionalidades. Explica de manera clara y explicita qué hace el proyecto y por qué es importante.
    
3.  **Instrucciones de instalación**: Proporciona instrucciones detalladas sobre cómo instalar y configurar el proyecto. Incluye los requisitos previos y los pasos necesarios para que otras personas puedan ejecutar el proyecto en sus propios entornos.
    
4.  **Uso del proyecto:** Describe cómo utilizar el proyecto una vez instalado. Proporciona ejemplos de comandos, configuraciones o cualquier otra información relevante para que los usuarios puedan aprovechar al máximo el proyecto.
    
5.  **Estructura del proyecto:** Si el proyecto tiene una estructura específica de carpetas o archivos, explícala brevemente para que los usuarios puedan encontrar y navegar. **(MVC)**
    
6.  **Dependencias y requisitos:** Enumera todas las dependencias externas necesarias para el proyecto, como bibliotecas, frameworks o herramientas adicionales. 

 7.  **Contacto:** Proporciona información de contacto, como tu dirección de correo electrónico o enlaces a tus perfiles en redes sociales, para que los usuarios y/o interesados puedan comunicarse contigo ..


