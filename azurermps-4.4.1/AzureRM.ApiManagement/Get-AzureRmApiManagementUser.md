---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573776"
---
# <span data-ttu-id="8ab5f-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="8ab5f-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="8ab5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ab5f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab5f-103">Hämtar en användare eller användare.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ab5f-104">SYNTAX</span></span>

### <span data-ttu-id="8ab5f-105">Hämta alla användare (standard)</span><span class="sxs-lookup"><span data-stu-id="8ab5f-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ab5f-106">Skaffa användare utifrån ID</span><span class="sxs-lookup"><span data-stu-id="8ab5f-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ab5f-107">Hitta användare</span><span class="sxs-lookup"><span data-stu-id="8ab5f-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab5f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ab5f-108">DESCRIPTION</span></span>
<span data-ttu-id="8ab5f-109">Cmdleten **Get-AzureRmApiManagementUser** hämtar en angiven användare eller alla användare om ingen användare har angetts.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="8ab5f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ab5f-110">EXAMPLES</span></span>

### <span data-ttu-id="8ab5f-111">Exempel 1: Hämta alla användare</span><span class="sxs-lookup"><span data-stu-id="8ab5f-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="8ab5f-112">Det här kommandot får alla användare.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-112">This command gets all users.</span></span>

### <span data-ttu-id="8ab5f-113">Exempel 2: skaffa en användare utifrån ID</span><span class="sxs-lookup"><span data-stu-id="8ab5f-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="8ab5f-114">Det här kommandot får en användare via ID.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="8ab5f-115">Exempel: Hämta användare efter efter namn</span><span class="sxs-lookup"><span data-stu-id="8ab5f-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="8ab5f-116">Med det här kommandot får du användare med ett angivet efter namn, fullständig Nilsson.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="8ab5f-117">Exempel 4: Hämta en användare via e-postadress</span><span class="sxs-lookup"><span data-stu-id="8ab5f-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="8ab5f-118">Det här kommandot får användaren som har angiven e-postadress.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="8ab5f-119">Exempel 5: samla alla användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="8ab5f-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="8ab5f-120">Det här kommandot får alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="8ab5f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ab5f-121">PARAMETERS</span></span>

### <span data-ttu-id="8ab5f-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8ab5f-122">-Context</span></span>
<span data-ttu-id="8ab5f-123">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="8ab5f-124">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="8ab5f-124">-Email</span></span>
<span data-ttu-id="8ab5f-125">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="8ab5f-126">Om den här parametern anges hittas en användare via e-post.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="8ab5f-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="8ab5f-128">-FirstName</span></span>
<span data-ttu-id="8ab5f-129">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="8ab5f-130">Om denna parameter anges hittar denna cmdlet en användare via förnamnet.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="8ab5f-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-132">-Kund-</span><span class="sxs-lookup"><span data-stu-id="8ab5f-132">-GroupId</span></span>
<span data-ttu-id="8ab5f-133">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-133">Specifies the group identifier.</span></span>
<span data-ttu-id="8ab5f-134">Om den anges hittar denna cmdlet alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="8ab5f-135">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="8ab5f-136">-LastName</span></span>
<span data-ttu-id="8ab5f-137">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="8ab5f-138">Om den här cmdleten anges hittas användare med efter namn.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="8ab5f-139">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-140">-State</span><span class="sxs-lookup"><span data-stu-id="8ab5f-140">-State</span></span>
<span data-ttu-id="8ab5f-141">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-141">Specifies the user state.</span></span>
<span data-ttu-id="8ab5f-142">Om det här alternativet anges hittar denna cmdlet användare i det här tillståndet.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="8ab5f-143">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="8ab5f-144">-UserId</span></span>
<span data-ttu-id="8ab5f-145">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-145">Specifies a user ID.</span></span>
<span data-ttu-id="8ab5f-146">Om det här alternativet anges hittar denna cmdlet användaren med den här identifieraren.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="8ab5f-147">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab5f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab5f-148">-DefaultProfile</span></span>
<span data-ttu-id="8ab5f-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ab5f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab5f-150">CommonParameters</span></span>
<span data-ttu-id="8ab5f-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab5f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab5f-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab5f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab5f-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ab5f-153">INPUTS</span></span>

## <span data-ttu-id="8ab5f-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ab5f-154">OUTPUTS</span></span>

### <span data-ttu-id="8ab5f-155">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="8ab5f-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="8ab5f-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ab5f-156">NOTES</span></span>

## <span data-ttu-id="8ab5f-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ab5f-157">RELATED LINKS</span></span>

[<span data-ttu-id="8ab5f-158">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="8ab5f-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="8ab5f-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="8ab5f-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="8ab5f-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="8ab5f-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


