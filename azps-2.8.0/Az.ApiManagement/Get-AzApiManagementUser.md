---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 6a242334378ceade2f786873181c68f04f8b09a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745810"
---
# <span data-ttu-id="326b4-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="326b4-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="326b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="326b4-102">SYNOPSIS</span></span>
<span data-ttu-id="326b4-103">Hämtar en användare eller användare.</span><span class="sxs-lookup"><span data-stu-id="326b4-103">Gets a user or users.</span></span>

## <span data-ttu-id="326b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="326b4-104">SYNTAX</span></span>

### <span data-ttu-id="326b4-105">GeAllUsers (standard)</span><span class="sxs-lookup"><span data-stu-id="326b4-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="326b4-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="326b4-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="326b4-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="326b4-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="326b4-108">DESCRIPTION</span></span>
<span data-ttu-id="326b4-109">Cmdleten **Get-AzApiManagementUser** hämtar en angiven användare eller alla användare om ingen användare har angetts.</span><span class="sxs-lookup"><span data-stu-id="326b4-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="326b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="326b4-110">EXAMPLES</span></span>

### <span data-ttu-id="326b4-111">Exempel 1: Hämta alla användare</span><span class="sxs-lookup"><span data-stu-id="326b4-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="326b4-112">Det här kommandot får alla användare.</span><span class="sxs-lookup"><span data-stu-id="326b4-112">This command gets all users.</span></span>

### <span data-ttu-id="326b4-113">Exempel 2: skaffa en användare utifrån ID</span><span class="sxs-lookup"><span data-stu-id="326b4-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="326b4-114">Det här kommandot får en användare via ID.</span><span class="sxs-lookup"><span data-stu-id="326b4-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="326b4-115">Exempel: Hämta användare efter efter namn</span><span class="sxs-lookup"><span data-stu-id="326b4-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="326b4-116">Med det här kommandot får du användare med ett angivet efter namn, fullständig Nilsson.</span><span class="sxs-lookup"><span data-stu-id="326b4-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="326b4-117">Exempel 4: Hämta en användare via e-postadress</span><span class="sxs-lookup"><span data-stu-id="326b4-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="326b4-118">Det här kommandot får användaren som har angiven e-postadress.</span><span class="sxs-lookup"><span data-stu-id="326b4-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="326b4-119">Exempel 5: samla alla användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="326b4-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="326b4-120">Det här kommandot får alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="326b4-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="326b4-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="326b4-121">PARAMETERS</span></span>

### <span data-ttu-id="326b4-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="326b4-122">-Context</span></span>
<span data-ttu-id="326b4-123">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="326b4-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="326b4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326b4-124">-DefaultProfile</span></span>
<span data-ttu-id="326b4-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="326b4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326b4-126">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="326b4-126">-Email</span></span>
<span data-ttu-id="326b4-127">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="326b4-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="326b4-128">Om den här parametern anges hittas en användare via e-post.</span><span class="sxs-lookup"><span data-stu-id="326b4-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="326b4-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="326b4-130">-FirstName</span></span>
<span data-ttu-id="326b4-131">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="326b4-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="326b4-132">Om denna parameter anges hittar denna cmdlet en användare via förnamnet.</span><span class="sxs-lookup"><span data-stu-id="326b4-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="326b4-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-134">-Kund-</span><span class="sxs-lookup"><span data-stu-id="326b4-134">-GroupId</span></span>
<span data-ttu-id="326b4-135">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="326b4-135">Specifies the group identifier.</span></span>
<span data-ttu-id="326b4-136">Om den anges hittar denna cmdlet alla användare i den angivna gruppen.</span><span class="sxs-lookup"><span data-stu-id="326b4-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="326b4-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="326b4-138">-LastName</span></span>
<span data-ttu-id="326b4-139">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="326b4-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="326b4-140">Om den här cmdleten anges hittas användare med efter namn.</span><span class="sxs-lookup"><span data-stu-id="326b4-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="326b4-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-142">-State</span><span class="sxs-lookup"><span data-stu-id="326b4-142">-State</span></span>
<span data-ttu-id="326b4-143">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="326b4-143">Specifies the user state.</span></span>
<span data-ttu-id="326b4-144">Om det här alternativet anges hittar denna cmdlet användare i det här tillståndet.</span><span class="sxs-lookup"><span data-stu-id="326b4-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="326b4-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="326b4-146">-UserId</span></span>
<span data-ttu-id="326b4-147">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="326b4-147">Specifies a user ID.</span></span>
<span data-ttu-id="326b4-148">Om det här alternativet anges hittar denna cmdlet användaren med den här identifieraren.</span><span class="sxs-lookup"><span data-stu-id="326b4-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="326b4-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="326b4-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="326b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326b4-150">CommonParameters</span></span>
<span data-ttu-id="326b4-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326b4-152">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="326b4-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326b4-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="326b4-153">INPUTS</span></span>

### <span data-ttu-id="326b4-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="326b4-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="326b4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="326b4-155">System.String</span></span>

### <span data-ttu-id="326b4-156">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="326b4-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="326b4-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="326b4-157">OUTPUTS</span></span>

### <span data-ttu-id="326b4-158">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="326b4-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="326b4-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="326b4-159">NOTES</span></span>

## <span data-ttu-id="326b4-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="326b4-160">RELATED LINKS</span></span>

[<span data-ttu-id="326b4-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="326b4-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="326b4-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="326b4-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="326b4-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="326b4-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


