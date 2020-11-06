---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 07bc19bd2314164b37ec9e014f5cad68de97d21f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576104"
---
# <span data-ttu-id="b89b4-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b89b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b89b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b89b4-103">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="b89b4-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b89b4-104">SYNTAX</span></span>

### <span data-ttu-id="b89b4-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b89b4-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89b4-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89b4-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89b4-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89b4-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89b4-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89b4-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89b4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89b4-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b89b4-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b89b4-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b89b4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b89b4-111">DESCRIPTION</span></span>
<span data-ttu-id="b89b4-112">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="b89b4-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="b89b4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b89b4-113">EXAMPLES</span></span>

### <span data-ttu-id="b89b4-114">Exempel 1 – ta bort ett tjänst huvud objekt efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="b89b4-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="b89b4-115">Tar bort tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 '.</span><span class="sxs-lookup"><span data-stu-id="b89b4-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="b89b4-116">Exempel 2 – ta bort ett tjänst huvud baserat på program-ID</span><span class="sxs-lookup"><span data-stu-id="b89b4-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="b89b4-117">Tar bort tjänstens huvud namn med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 '.</span><span class="sxs-lookup"><span data-stu-id="b89b4-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="b89b4-118">Exempel 3 – ta bort ett tjänst huvud med SPN</span><span class="sxs-lookup"><span data-stu-id="b89b4-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="b89b4-119">Ta bort tjänstens huvud namn med SPN "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="b89b4-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="b89b4-120">Exempel 4 – ta bort ett tjänst huvud genom rör</span><span class="sxs-lookup"><span data-stu-id="b89b4-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="b89b4-121">Hämtar tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' och pipes till Remove-AzureRmADServicePrincipal cmdlet för att ta bort tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b89b4-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="b89b4-122">Exempel 5 – ta bort ett tjänst huvud genom att rikta ett program</span><span class="sxs-lookup"><span data-stu-id="b89b4-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="b89b4-123">Hämtar programmet med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 ' och rör till cmdleten Remove-AzureRmADServicePrincipal för att ta bort tjänstens huvud objekt som är associerat med det programmet.</span><span class="sxs-lookup"><span data-stu-id="b89b4-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="b89b4-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b89b4-124">PARAMETERS</span></span>

### <span data-ttu-id="b89b4-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b89b4-125">-ApplicationId</span></span>
<span data-ttu-id="b89b4-126">Tjänstens huvud program-ID.</span><span class="sxs-lookup"><span data-stu-id="b89b4-126">The service principal application id.</span></span>

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

### <span data-ttu-id="b89b4-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b89b4-127">-ApplicationObject</span></span>
<span data-ttu-id="b89b4-128">Program objekt vars tjänste huvud ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b89b4-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89b4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89b4-129">-DefaultProfile</span></span>
<span data-ttu-id="b89b4-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b89b4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b89b4-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b89b4-131">-DisplayName</span></span>
<span data-ttu-id="b89b4-132">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="b89b4-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="b89b4-133">-Force</span><span class="sxs-lookup"><span data-stu-id="b89b4-133">-Force</span></span>
<span data-ttu-id="b89b4-134">Växla till att ta bort tjänstens huvud konto utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b89b4-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="b89b4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b89b4-135">-InputObject</span></span>
<span data-ttu-id="b89b4-136">Tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b89b4-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89b4-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b89b4-137">-ObjectId</span></span>
<span data-ttu-id="b89b4-138">Objekt-ID för det tjänst objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b89b4-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89b4-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b89b4-139">-PassThru</span></span>
<span data-ttu-id="b89b4-140">Om det anges returneras den borttagna tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="b89b4-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="b89b4-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b89b4-141">-ServicePrincipalName</span></span>
<span data-ttu-id="b89b4-142">Tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="b89b4-142">The service principal name.</span></span>

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

### <span data-ttu-id="b89b4-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b89b4-143">-Confirm</span></span>
<span data-ttu-id="b89b4-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b89b4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89b4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89b4-145">-WhatIf</span></span>
<span data-ttu-id="b89b4-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b89b4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b89b4-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b89b4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89b4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89b4-148">CommonParameters</span></span>
<span data-ttu-id="b89b4-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89b4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89b4-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89b4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89b4-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b89b4-151">INPUTS</span></span>

### <span data-ttu-id="b89b4-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b89b4-152">System.Guid</span></span>

### <span data-ttu-id="b89b4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b89b4-153">System.String</span></span>

### <span data-ttu-id="b89b4-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="b89b4-155">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b89b4-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b89b4-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b89b4-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="b89b4-157">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b89b4-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="b89b4-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b89b4-158">OUTPUTS</span></span>

### <span data-ttu-id="b89b4-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b89b4-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b89b4-160">NOTES</span></span>
<span data-ttu-id="b89b4-161">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b89b4-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b89b4-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b89b4-162">RELATED LINKS</span></span>

[<span data-ttu-id="b89b4-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b89b4-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b89b4-165">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b89b4-165">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b89b4-166">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b89b4-166">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b89b4-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b89b4-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
