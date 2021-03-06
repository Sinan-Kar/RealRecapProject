[![GitHub License](https://img.shields.io/github/license/Sinan-Kar/RealRecapProject?color=green)](https://github.com/Sinan-Kar/RealRecapProject/blob/master/LICENSE.txt)
![GitHub repo size](https://img.shields.io/github/repo-size/Sinan-Kar/RealRecapProject)

<h1 align="center">ReCap Project : Araba Kiralama Sistemi</h1> 

![Image for Usage](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/images/recap.png)
## ⭐ Introduction 
- **Entities, DataAccess, Business ve Console katmanlarından oluşan araba kiralama console projesidir. Car, Brand, Color, Customer, User, CarImages ve Rental nesnelerinden ve onun operasyonlarından oluşur.**
- **[Sql query](https://github.com/Sinan-Kar/RealRecapProject/blob/master/RentACarSQLQuery.sql) dosyamı da ekledim isteyen varsa faydalanabilir.**


## Recent Changes
✔ AOP yaklaşımında CastleDynamicProxy kullanıldı.Bir IoC Container olan Autofac’ten yararlanıldı.<br>
✔ Dependency Injection Autofac ile uygulandı.<br>
✔ Caching, JsonWebTokin, Transaction ve Performance aspectleri eklendi. <br>
✔ CarManager class'ına ait olan GetAll metoduna Logging aspect'i eklendi. <br>
✔ Car nesnesinin GetAll metodu performance ile test edildi. <br>
✔ Çalıştırılan metodlar log4net.config ile log.json dosyasına yazıldı. <br> 

## Table of Contents
- [Recent Changes](#recent-changes)
- [Usage](#usage)
- [Layers](#layers)
- [SQL Query](#sql-query)
- [Tables in Database](#tables-in-database)
- [Output](#output)
- [Files](#files)


## Usage 
Aşağıda görmüş olduğunuz resimdeki işlemi gerçekleştirdikten sonra Ctrl+F5 ile uygulamayı çalıştırabilirsiniz.

![Image for Usage](https://user-images.githubusercontent.com/43720773/107143179-aa40d400-6944-11eb-9a45-e3f6dcdf6b80.jpg)


## Layers
🗃 **``Entities Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Concrete`` <br>                   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Brand.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/Brand.cs)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Car.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/Car.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarImage.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/CarImage.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Color.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/Color.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Customer.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/Customer.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Rental.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/Rental.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [User.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/Concrete/User.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``DTOs`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarDetailDto.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/DTOs/CarDetailDto.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [RentalDetailDto.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Entities/DTOs/RentalDetailDto.cs) <br><br>

🗃 **``Business Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Abstract`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IBrandService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/IBrandService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICarImageService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/ICarImageService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICarService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/ICarService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IColorService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/IColorService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICustomerService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/ICustomerService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IRentalService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/IRentalService.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IUserService.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Abstract/IUserService.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Concrete`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [BrandManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/BrandManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarImageManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/CarImageManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/CarManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ColorManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/ColorManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CustomerManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/CustomerManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [RentalManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/RentalManager.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [UserManager.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Concrete/UserManager.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Constants`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Messages.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/Constants/Messages.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``DependencyResolvers`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Autofac`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [AutofacBusinessModule.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/DependencyResolvers/Autofac/AutofacBusinessModule.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``ValidationRules`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``FluentValidation`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [BrandValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/BrandValidator.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/CarValidator.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ColorValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/ColorValidator.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CustomerValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/CustomerValidator.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [RentalValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/RentalValidator.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [UserValidator.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Business/ValidationRules/FluentValidation/UserValidator.cs) <br><br>


🗃 **``Data Access Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Abstract`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IBrandDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/IBrandDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICarImageDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/ICarImageDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICarDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/ICarDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IColorDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/IColorDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ICustomerDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/ICustomerDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IRentalDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/IRentalDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IUserDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Abstract/IUserDal.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Concrete`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``EntityFramework`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Context`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [RentACarContext.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Context/RentACarContext.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📂 ``Repository`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfBrandDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfBrandDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfCarImageDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfCarImageDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfCarDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfCarDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfColorDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfColorDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfCustomerDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfCustomerDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfRentalDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfRentalDal.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  📃 [EfUserDal.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/DataAccess/Concrete/EntityFramework/Repository/EfUserDal.cs) <br><br>


🗃 **``Core Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Aspect`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Autofac`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Validation`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ValidationAspect.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Aspects/Autofac/Validation/ValidationAspect.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``CrossCuttingConcerns`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Validation`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📃 [ValidationTool.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/CrossCuttingConcerns/Validation/ValidationTool.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``DataAccess`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IEntityRepository.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/DataAccess/IEntityRepository.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``EntityFramework`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [EfEntityRepositoryBase.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/DataAccess/EntityFramework/EfEntityRepositoryBase.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Entities`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IDto.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Entities/IDto.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IEntity.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Entities/IEntity.cs) <br>

&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Utilities`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Business`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [BusinessRules.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Business/BusinessRules.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``FileHelper`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [FileHelper.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/FileHelper/FileHelper.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Interceptors`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [AspectInterceptorSelector.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Interceptors/AspectInterceptorSelector.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [MethodInterception.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Interceptors/MethodInterception.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [MethodInterceptionBaseAttribute.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Interceptors/MethodInterceptionBaseAttribute.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Results`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IDataResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/DataResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [DataResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/DataResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [SuccessDataResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/SuccessDataResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ErrorDataResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/ErrorDataResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [IResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/IResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Result.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/Result.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [SuccessResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/SuccessResult.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ErrorResult.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/Core/Utilities/Results/ErrorResult.cs) <br><br>


🗃 **``Presentation Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp; 📃 [Program.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/ConsoleUI/Program.cs)<br><br>

🗃 **``WebAPI Layer``** <br>
&nbsp;&nbsp;&nbsp;&nbsp;📃 [Startup.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Startup.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;📂 ``Controllers`` <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [BrandsController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/BrandsController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarImagesController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/CarImagesController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CarsController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/CarsController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [ColorsController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/ColorsController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [CustomersController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/CustomersController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [RentalsController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/RentalsController.cs) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 📃 [UsersController.cs](https://github.com/Sinan-Kar/RealRecapProject/blob/master/WebAPI/Controllers/UsersController.cs) <br><br>

## SQL Query
&nbsp;&nbsp;&nbsp;&nbsp; 📃 [RentACarSQLQuery.sql](https://github.com/Sinan-Kar/RealRecapProject/blob/master/RentACarSQLQuery.sql)


## Tables in Database
<table>
  <tr>
    <td>Cars</td>
     <td>Brands</td>
     <td>Colors</td>
  </tr>
  <tr>
    <td>

Variable Name | Data Type
------------ | -------------
CarId | int
BrandId | int
ColorId | int
ModelYear | nvarchar(25)
DailyPrice | decimal
Description | nvarchar(25)
   
   </td>
    <td>

Variable Name | Data Type
------------ | -------------
ColorId | int
ColorName | nvarchar(25)
   
   </td>
    <td>

Variable Name | Data Type
------------ | -------------
BrandId | int
BrandName | nvarchar(25)
   
   </td>
  </tr>
 </table>
 
 <table>
  <tr>
    <td>Customers</td>
     <td>Rentals</td>
     <td>Users</td>
     <td>CarImages</td>
  </tr>
  <tr>
    <td>

Variable Name | Data Type
------------ | -------------
CustomerId | int
UserId | int
CustomerName | nvarchar(25)
   
   </td>
    <td>

Variable Name | Data Type
------------ | -------------
RentalId | int
CarId | int
CustomerId | int
RentDate | datetime
ReturnDate | datetime

   </td>
    <td>

Variable Name | Data Type
------------ | -------------
UserId | int
FirstName | nvarchar(25)
LastName | nvarchar(25)
Email | nvarchar(55)
Password | nvarchar(35)

   </td>
   <td>

Variable Name | Data Type
------------ | -------------
CarImagesId | int
CarId | int
CarImagesDate | datetime
ImagePath | nvarchar(MAX)

   </td>
  </tr>
 </table>

## Output
<img src="https://user-images.githubusercontent.com/43720773/107849881-381e3280-6e0f-11eb-848d-14c5fc54a4e9.jpg" alt="Console Output"></img>


## Files

<img src="https://user-images.githubusercontent.com/43720773/108479671-0e4d8b80-72a7-11eb-907f-0dfcc2a1eac7.jpg"></img><br>
<img src="https://user-images.githubusercontent.com/43720773/108479673-0ee62200-72a7-11eb-9685-e044171df607.jpg"></img><br>
<img src="https://user-images.githubusercontent.com/43720773/108479675-0f7eb880-72a7-11eb-86a6-3f48c0429e9f.jpg"></img><br>
<img src="https://user-images.githubusercontent.com/43720773/108479677-0f7eb880-72a7-11eb-9ac8-7c9edd91f1e1.jpg"></img><br>
<img src="https://user-images.githubusercontent.com/43720773/108479679-10174f00-72a7-11eb-9bc3-0590da8dfc2c.jpg"></img><br>
<img src="https://user-images.githubusercontent.com/43720773/108479681-10174f00-72a7-11eb-8140-8b98e38dc077.jpg"></img>


#### :pencil2:Authors
* **Sinan Kara** - [Sinan Kara](https://github.com/Sinan-Kar)
*/
 
