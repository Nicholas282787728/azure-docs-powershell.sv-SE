---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 7f306503754ca945ab4abb001cf08f8574b67025
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521323"
---
# <span data-ttu-id="d0236-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="d0236-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0236-102">SYNOPSIS</span></span>
<span data-ttu-id="d0236-103">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="d0236-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="d0236-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0236-104">SYNTAX</span></span>

### <span data-ttu-id="d0236-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0236-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0236-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0236-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0236-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0236-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0236-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0236-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0236-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0236-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0236-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0236-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0236-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0236-111">DESCRIPTION</span></span>
<span data-ttu-id="d0236-112">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="d0236-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="d0236-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0236-113">EXAMPLES</span></span>

### <span data-ttu-id="d0236-114">Exempel 1 – ta bort ett tjänst huvud objekt efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="d0236-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="d0236-115">Tar bort tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 '.</span><span class="sxs-lookup"><span data-stu-id="d0236-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="d0236-116">Exempel 2 – ta bort ett tjänst huvud baserat på program-ID</span><span class="sxs-lookup"><span data-stu-id="d0236-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="d0236-117">Tar bort tjänstens huvud namn med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 '.</span><span class="sxs-lookup"><span data-stu-id="d0236-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="d0236-118">Exempel 3 – ta bort ett tjänst huvud med SPN</span><span class="sxs-lookup"><span data-stu-id="d0236-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="d0236-119">Ta bort tjänstens huvud namn med SPN "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="d0236-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="d0236-120">Exempel 4 – ta bort ett tjänst huvud genom rör</span><span class="sxs-lookup"><span data-stu-id="d0236-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="d0236-121">Hämtar tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' och pipes till Remove-AzADServicePrincipal cmdlet för att ta bort tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="d0236-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="d0236-122">Exempel 5 – ta bort ett tjänst huvud genom att rikta ett program</span><span class="sxs-lookup"><span data-stu-id="d0236-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="d0236-123">Hämtar programmet med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 ' och rör till cmdleten Remove-AzADServicePrincipal för att ta bort tjänstens huvud objekt som är associerat med det programmet.</span><span class="sxs-lookup"><span data-stu-id="d0236-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="d0236-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0236-124">PARAMETERS</span></span>

### <span data-ttu-id="d0236-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d0236-125">-ApplicationId</span></span>
<span data-ttu-id="d0236-126">Tjänstens huvud program-ID.</span><span class="sxs-lookup"><span data-stu-id="d0236-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d0236-127">-ApplicationObject</span></span>
<span data-ttu-id="d0236-128">Program objekt vars tjänste huvud ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d0236-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0236-129">-DefaultProfile</span></span>
<span data-ttu-id="d0236-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0236-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0236-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d0236-131">-DisplayName</span></span>
<span data-ttu-id="d0236-132">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="d0236-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-133">-Force</span><span class="sxs-lookup"><span data-stu-id="d0236-133">-Force</span></span>
<span data-ttu-id="d0236-134">Växla till att ta bort tjänstens huvud konto utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d0236-134">Switch to delete service principal without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0236-135">-InputObject</span></span>
<span data-ttu-id="d0236-136">Tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="d0236-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d0236-137">-ObjectId</span></span>
<span data-ttu-id="d0236-138">Objekt-ID för det tjänst objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d0236-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0236-139">-PassThru</span></span>
<span data-ttu-id="d0236-140">Om det anges returneras den borttagna tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d0236-140">If specified, returns the deleted service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0236-141">-ServicePrincipalName</span></span>
<span data-ttu-id="d0236-142">Tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d0236-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0236-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0236-143">-Confirm</span></span>
<span data-ttu-id="d0236-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0236-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0236-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0236-145">-WhatIf</span></span>
<span data-ttu-id="d0236-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0236-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0236-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0236-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0236-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0236-148">CommonParameters</span></span>
<span data-ttu-id="d0236-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0236-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0236-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0236-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0236-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0236-151">INPUTS</span></span>

### <span data-ttu-id="d0236-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d0236-152">System.String</span></span>

### <span data-ttu-id="d0236-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d0236-153">System.Guid</span></span>

### <span data-ttu-id="d0236-154">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d0236-155">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d0236-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d0236-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0236-156">OUTPUTS</span></span>

### <span data-ttu-id="d0236-157">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="d0236-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0236-158">NOTES</span></span>
<span data-ttu-id="d0236-159">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="d0236-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d0236-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0236-160">RELATED LINKS</span></span>

[<span data-ttu-id="d0236-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="d0236-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="d0236-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0236-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="d0236-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d0236-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d0236-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d0236-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
