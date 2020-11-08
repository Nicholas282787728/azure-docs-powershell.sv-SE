---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091894"
---
# <span data-ttu-id="52851-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52851-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="52851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52851-102">SYNOPSIS</span></span>
<span data-ttu-id="52851-103">Anger användar information.</span><span class="sxs-lookup"><span data-stu-id="52851-103">Sets user details.</span></span>

## <span data-ttu-id="52851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52851-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52851-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52851-105">DESCRIPTION</span></span>
<span data-ttu-id="52851-106">Cmdleten **set-AzApiManagementUser** anger användar information.</span><span class="sxs-lookup"><span data-stu-id="52851-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="52851-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52851-107">EXAMPLES</span></span>

### <span data-ttu-id="52851-108">Exempel 1: ändra en användares lösen ord, e-postadress och status</span><span class="sxs-lookup"><span data-stu-id="52851-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="52851-109">Det här kommandot anger ett nytt lösen ord och en e-postadress för användaren.</span><span class="sxs-lookup"><span data-stu-id="52851-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="52851-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52851-110">PARAMETERS</span></span>

### <span data-ttu-id="52851-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="52851-111">-Context</span></span>
<span data-ttu-id="52851-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="52851-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="52851-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="52851-113">This parameter is required.</span></span>

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

### <span data-ttu-id="52851-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52851-114">-DefaultProfile</span></span>
<span data-ttu-id="52851-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52851-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52851-116">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="52851-116">-Email</span></span>
<span data-ttu-id="52851-117">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="52851-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="52851-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="52851-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="52851-119">-FirstName</span></span>
<span data-ttu-id="52851-120">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="52851-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="52851-121">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="52851-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="52851-122">-LastName</span></span>
<span data-ttu-id="52851-123">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="52851-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="52851-124">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="52851-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-125">-Obs!</span><span class="sxs-lookup"><span data-stu-id="52851-125">-Note</span></span>
<span data-ttu-id="52851-126">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="52851-126">Specifies a note about the user.</span></span>
<span data-ttu-id="52851-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="52851-127">This parameter is optional.</span></span>
<span data-ttu-id="52851-128">Standardvärdet för den här parametern är $null.</span><span class="sxs-lookup"><span data-stu-id="52851-128">The default value of this parameter is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52851-129">-PassThru</span></span>
<span data-ttu-id="52851-130">passthru</span><span class="sxs-lookup"><span data-stu-id="52851-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-131">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="52851-131">-Password</span></span>
<span data-ttu-id="52851-132">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="52851-132">Specifies the user password.</span></span>
<span data-ttu-id="52851-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="52851-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-134">-State</span><span class="sxs-lookup"><span data-stu-id="52851-134">-State</span></span>
<span data-ttu-id="52851-135">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="52851-135">Specifies the user state.</span></span>
<span data-ttu-id="52851-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="52851-136">This parameter is optional.</span></span>
<span data-ttu-id="52851-137">Standardvärdet är aktivt.</span><span class="sxs-lookup"><span data-stu-id="52851-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="52851-138">-UserId</span></span>
<span data-ttu-id="52851-139">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="52851-139">Specifies the user ID.</span></span>
<span data-ttu-id="52851-140">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="52851-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52851-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52851-141">-Confirm</span></span>
<span data-ttu-id="52851-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52851-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52851-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52851-143">-WhatIf</span></span>
<span data-ttu-id="52851-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52851-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52851-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52851-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52851-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52851-146">CommonParameters</span></span>
<span data-ttu-id="52851-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52851-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52851-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52851-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52851-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52851-149">INPUTS</span></span>

### <span data-ttu-id="52851-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52851-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52851-151">System. String</span><span class="sxs-lookup"><span data-stu-id="52851-151">System.String</span></span>

### <span data-ttu-id="52851-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="52851-152">System.Security.SecureString</span></span>

### <span data-ttu-id="52851-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="52851-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="52851-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52851-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52851-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52851-155">OUTPUTS</span></span>

### <span data-ttu-id="52851-156">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52851-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="52851-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52851-157">NOTES</span></span>

## <span data-ttu-id="52851-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52851-158">RELATED LINKS</span></span>

[<span data-ttu-id="52851-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52851-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="52851-160">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52851-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="52851-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52851-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


