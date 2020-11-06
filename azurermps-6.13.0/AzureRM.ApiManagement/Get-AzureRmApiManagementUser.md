---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579124"
---
# <span data-ttu-id="7675b-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7675b-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="7675b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7675b-102">SYNOPSIS</span></span>
<span data-ttu-id="7675b-103">Hämtar en användare eller användare.</span><span class="sxs-lookup"><span data-stu-id="7675b-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7675b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7675b-104">SYNTAX</span></span>

### <span data-ttu-id="7675b-105">GeAllUsers (standard)</span><span class="sxs-lookup"><span data-stu-id="7675b-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7675b-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="7675b-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7675b-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="7675b-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7675b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7675b-108">DESCRIPTION</span></span>
<span data-ttu-id="7675b-109">Cmdleten **Get-AzureRmApiManagementUser** hämtar en angiven användare eller alla användare om ingen användare har angetts.</span><span class="sxs-lookup"><span data-stu-id="7675b-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="7675b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7675b-110">EXAMPLES</span></span>

### <span data-ttu-id="7675b-111">Exempel 1: Hämta alla användare</span><span class="sxs-lookup"><span data-stu-id="7675b-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="7675b-112">Det här kommandot får alla användare.</span><span class="sxs-lookup"><span data-stu-id="7675b-112">This command gets all users.</span></span>

### <span data-ttu-id="7675b-113">Exempel 2: skaffa en användare utifrån ID</span><span class="sxs-lookup"><span data-stu-id="7675b-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="7675b-114">Det här kommandot får en användare via ID.</span><span class="sxs-lookup"><span data-stu-id="7675b-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="7675b-115">Exempel: Hämta användare efter efter namn</span><span class="sxs-lookup"><span data-stu-id="7675b-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="7675b-116">Med det här kommandot får du användare med ett angivet efter namn, fullständig Nilsson.</span><span class="sxs-lookup"><span data-stu-id="7675b-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="7675b-117">Exempel 4: Hämta en användare via e-postadress</span><span class="sxs-lookup"><span data-stu-id="7675b-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="7675b-118">Det här kommandot får användaren som har angiven e-postadress.</span><span class="sxs-lookup"><span data-stu-id="7675b-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="7675b-119">Exempel 5: samla alla användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="7675b-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="7675b-120">Det här kommandot får alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="7675b-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="7675b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7675b-121">PARAMETERS</span></span>

### <span data-ttu-id="7675b-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7675b-122">-Context</span></span>
<span data-ttu-id="7675b-123">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="7675b-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7675b-124">-DefaultProfile</span></span>
<span data-ttu-id="7675b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7675b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-126">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="7675b-126">-Email</span></span>
<span data-ttu-id="7675b-127">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="7675b-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="7675b-128">Om den här parametern anges hittas en användare via e-post.</span><span class="sxs-lookup"><span data-stu-id="7675b-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="7675b-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7675b-130">-FirstName</span></span>
<span data-ttu-id="7675b-131">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="7675b-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="7675b-132">Om denna parameter anges hittar denna cmdlet en användare via förnamnet.</span><span class="sxs-lookup"><span data-stu-id="7675b-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="7675b-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-134">-Kund-</span><span class="sxs-lookup"><span data-stu-id="7675b-134">-GroupId</span></span>
<span data-ttu-id="7675b-135">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="7675b-135">Specifies the group identifier.</span></span>
<span data-ttu-id="7675b-136">Om den anges hittar denna cmdlet alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="7675b-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="7675b-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="7675b-138">-LastName</span></span>
<span data-ttu-id="7675b-139">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="7675b-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="7675b-140">Om den här cmdleten anges hittas användare med efter namn.</span><span class="sxs-lookup"><span data-stu-id="7675b-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="7675b-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-142">-State</span><span class="sxs-lookup"><span data-stu-id="7675b-142">-State</span></span>
<span data-ttu-id="7675b-143">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="7675b-143">Specifies the user state.</span></span>
<span data-ttu-id="7675b-144">Om det här alternativet anges hittar denna cmdlet användare i det här tillståndet.</span><span class="sxs-lookup"><span data-stu-id="7675b-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="7675b-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="7675b-146">-UserId</span></span>
<span data-ttu-id="7675b-147">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="7675b-147">Specifies a user ID.</span></span>
<span data-ttu-id="7675b-148">Om det här alternativet anges hittar denna cmdlet användaren med den här identifieraren.</span><span class="sxs-lookup"><span data-stu-id="7675b-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="7675b-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7675b-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7675b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7675b-150">CommonParameters</span></span>
<span data-ttu-id="7675b-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7675b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7675b-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7675b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7675b-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7675b-153">INPUTS</span></span>

### <span data-ttu-id="7675b-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7675b-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7675b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7675b-155">System.String</span></span>

### <span data-ttu-id="7675b-156">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7675b-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7675b-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7675b-157">OUTPUTS</span></span>

### <span data-ttu-id="7675b-158">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7675b-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="7675b-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7675b-159">NOTES</span></span>

## <span data-ttu-id="7675b-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7675b-160">RELATED LINKS</span></span>

[<span data-ttu-id="7675b-161">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7675b-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="7675b-162">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7675b-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="7675b-163">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7675b-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


