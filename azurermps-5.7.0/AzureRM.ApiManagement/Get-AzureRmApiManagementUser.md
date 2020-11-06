---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576651"
---
# <span data-ttu-id="ac469-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ac469-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="ac469-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac469-102">SYNOPSIS</span></span>
<span data-ttu-id="ac469-103">Hämtar en användare eller användare.</span><span class="sxs-lookup"><span data-stu-id="ac469-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac469-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac469-104">SYNTAX</span></span>

### <span data-ttu-id="ac469-105">GeAllUsers (standard)</span><span class="sxs-lookup"><span data-stu-id="ac469-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac469-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ac469-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac469-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="ac469-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac469-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac469-108">DESCRIPTION</span></span>
<span data-ttu-id="ac469-109">Cmdleten **Get-AzureRmApiManagementUser** hämtar en angiven användare eller alla användare om ingen användare har angetts.</span><span class="sxs-lookup"><span data-stu-id="ac469-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="ac469-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac469-110">EXAMPLES</span></span>

### <span data-ttu-id="ac469-111">Exempel 1: Hämta alla användare</span><span class="sxs-lookup"><span data-stu-id="ac469-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="ac469-112">Det här kommandot får alla användare.</span><span class="sxs-lookup"><span data-stu-id="ac469-112">This command gets all users.</span></span>

### <span data-ttu-id="ac469-113">Exempel 2: skaffa en användare utifrån ID</span><span class="sxs-lookup"><span data-stu-id="ac469-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ac469-114">Det här kommandot får en användare via ID.</span><span class="sxs-lookup"><span data-stu-id="ac469-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="ac469-115">Exempel: Hämta användare efter efter namn</span><span class="sxs-lookup"><span data-stu-id="ac469-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="ac469-116">Med det här kommandot får du användare med ett angivet efter namn, fullständig Nilsson.</span><span class="sxs-lookup"><span data-stu-id="ac469-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="ac469-117">Exempel 4: Hämta en användare via e-postadress</span><span class="sxs-lookup"><span data-stu-id="ac469-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="ac469-118">Det här kommandot får användaren som har angiven e-postadress.</span><span class="sxs-lookup"><span data-stu-id="ac469-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="ac469-119">Exempel 5: samla alla användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="ac469-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="ac469-120">Det här kommandot får alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="ac469-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="ac469-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac469-121">PARAMETERS</span></span>

### <span data-ttu-id="ac469-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ac469-122">-Context</span></span>
<span data-ttu-id="ac469-123">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ac469-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac469-124">-DefaultProfile</span></span>
<span data-ttu-id="ac469-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac469-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-126">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="ac469-126">-Email</span></span>
<span data-ttu-id="ac469-127">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="ac469-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="ac469-128">Om den här parametern anges hittas en användare via e-post.</span><span class="sxs-lookup"><span data-stu-id="ac469-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="ac469-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ac469-130">-FirstName</span></span>
<span data-ttu-id="ac469-131">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="ac469-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="ac469-132">Om denna parameter anges hittar denna cmdlet en användare via förnamnet.</span><span class="sxs-lookup"><span data-stu-id="ac469-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="ac469-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-134">-Kund-</span><span class="sxs-lookup"><span data-stu-id="ac469-134">-GroupId</span></span>
<span data-ttu-id="ac469-135">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="ac469-135">Specifies the group identifier.</span></span>
<span data-ttu-id="ac469-136">Om den anges hittar denna cmdlet alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="ac469-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="ac469-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="ac469-138">-LastName</span></span>
<span data-ttu-id="ac469-139">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="ac469-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="ac469-140">Om den här cmdleten anges hittas användare med efter namn.</span><span class="sxs-lookup"><span data-stu-id="ac469-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="ac469-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-142">-State</span><span class="sxs-lookup"><span data-stu-id="ac469-142">-State</span></span>
<span data-ttu-id="ac469-143">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ac469-143">Specifies the user state.</span></span>
<span data-ttu-id="ac469-144">Om det här alternativet anges hittar denna cmdlet användare i det här tillståndet.</span><span class="sxs-lookup"><span data-stu-id="ac469-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="ac469-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ac469-146">-UserId</span></span>
<span data-ttu-id="ac469-147">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="ac469-147">Specifies a user ID.</span></span>
<span data-ttu-id="ac469-148">Om det här alternativet anges hittar denna cmdlet användaren med den här identifieraren.</span><span class="sxs-lookup"><span data-stu-id="ac469-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="ac469-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ac469-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac469-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac469-150">CommonParameters</span></span>
<span data-ttu-id="ac469-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac469-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac469-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac469-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac469-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac469-153">INPUTS</span></span>

### <span data-ttu-id="ac469-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="ac469-154">None</span></span>
<span data-ttu-id="ac469-155">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ac469-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac469-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac469-156">OUTPUTS</span></span>

### <span data-ttu-id="ac469-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ac469-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="ac469-158">Information om användare i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ac469-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="ac469-159">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="ac469-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="ac469-160">Listan med användare i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ac469-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="ac469-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac469-161">NOTES</span></span>

## <span data-ttu-id="ac469-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac469-162">RELATED LINKS</span></span>

[<span data-ttu-id="ac469-163">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ac469-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="ac469-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ac469-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="ac469-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ac469-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


