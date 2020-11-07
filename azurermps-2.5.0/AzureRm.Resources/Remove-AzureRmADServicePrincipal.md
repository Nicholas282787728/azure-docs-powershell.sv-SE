---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928673"
---
# <span data-ttu-id="1b20d-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b20d-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="1b20d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b20d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b20d-103">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b20d-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b20d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b20d-104">SYNTAX</span></span>

### <span data-ttu-id="1b20d-105">ObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b20d-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b20d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b20d-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b20d-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b20d-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b20d-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b20d-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b20d-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b20d-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b20d-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b20d-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b20d-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b20d-111">DESCRIPTION</span></span>
<span data-ttu-id="1b20d-112">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b20d-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="1b20d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b20d-113">EXAMPLES</span></span>

### <span data-ttu-id="1b20d-114">Exempel 1 – ta bort ett tjänst huvud objekt efter objekt-ID</span><span class="sxs-lookup"><span data-stu-id="1b20d-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="1b20d-115">Tar bort tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 '.</span><span class="sxs-lookup"><span data-stu-id="1b20d-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="1b20d-116">Exempel 2 – ta bort ett tjänst huvud baserat på program-ID</span><span class="sxs-lookup"><span data-stu-id="1b20d-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="1b20d-117">Tar bort tjänstens huvud namn med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 '.</span><span class="sxs-lookup"><span data-stu-id="1b20d-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="1b20d-118">Exempel 3 – ta bort ett tjänst huvud med SPN</span><span class="sxs-lookup"><span data-stu-id="1b20d-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="1b20d-119">Ta bort tjänstens huvud namn med SPN "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="1b20d-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="1b20d-120">Exempel 4 – ta bort ett tjänst huvud genom rör</span><span class="sxs-lookup"><span data-stu-id="1b20d-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="1b20d-121">Hämtar tjänstens huvud namn med objekt-ID ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' och pipes till Remove-AzureRmADServicePrincipal cmdlet för att ta bort tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="1b20d-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="1b20d-122">Exempel 5 – ta bort ett tjänst huvud genom att rikta ett program</span><span class="sxs-lookup"><span data-stu-id="1b20d-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="1b20d-123">Hämtar programmet med program-ID ' 9263469e-d328-4321-8646-3e3e75d20e76 ' och rör till cmdleten Remove-AzureRmADServicePrincipal för att ta bort tjänstens huvud objekt som är associerat med det programmet.</span><span class="sxs-lookup"><span data-stu-id="1b20d-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="1b20d-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b20d-124">PARAMETERS</span></span>

### <span data-ttu-id="1b20d-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1b20d-125">-ApplicationId</span></span>
<span data-ttu-id="1b20d-126">Tjänstens huvud program-ID.</span><span class="sxs-lookup"><span data-stu-id="1b20d-126">The service principal application id.</span></span>

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

### <span data-ttu-id="1b20d-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1b20d-127">-ApplicationObject</span></span>
<span data-ttu-id="1b20d-128">Program objekt vars tjänste huvud ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1b20d-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="1b20d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b20d-129">-DefaultProfile</span></span>
<span data-ttu-id="1b20d-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1b20d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b20d-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b20d-131">-DisplayName</span></span>
<span data-ttu-id="1b20d-132">Visnings namnet på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="1b20d-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="1b20d-133">-Force</span><span class="sxs-lookup"><span data-stu-id="1b20d-133">-Force</span></span>
<span data-ttu-id="1b20d-134">Växla till att ta bort tjänstens huvud konto utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1b20d-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="1b20d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b20d-135">-InputObject</span></span>
<span data-ttu-id="1b20d-136">Tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="1b20d-136">The service principal object.</span></span>

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

### <span data-ttu-id="1b20d-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1b20d-137">-ObjectId</span></span>
<span data-ttu-id="1b20d-138">Objekt-ID för det tjänst objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1b20d-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="1b20d-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b20d-139">-PassThru</span></span>
<span data-ttu-id="1b20d-140">Om det anges returneras den borttagna tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="1b20d-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="1b20d-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1b20d-141">-ServicePrincipalName</span></span>
<span data-ttu-id="1b20d-142">Tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="1b20d-142">The service principal name.</span></span>

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

### <span data-ttu-id="1b20d-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b20d-143">-Confirm</span></span>
<span data-ttu-id="1b20d-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b20d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b20d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b20d-145">-WhatIf</span></span>
<span data-ttu-id="1b20d-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b20d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b20d-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b20d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b20d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b20d-148">CommonParameters</span></span>
<span data-ttu-id="1b20d-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b20d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b20d-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b20d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b20d-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b20d-151">INPUTS</span></span>

### <span data-ttu-id="1b20d-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1b20d-152">System.Guid</span></span>

### <span data-ttu-id="1b20d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1b20d-153">System.String</span></span>

### <span data-ttu-id="1b20d-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b20d-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="1b20d-155">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b20d-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1b20d-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1b20d-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1b20d-157">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b20d-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="1b20d-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b20d-158">OUTPUTS</span></span>

### <span data-ttu-id="1b20d-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b20d-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="1b20d-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b20d-160">NOTES</span></span>
<span data-ttu-id="1b20d-161">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="1b20d-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1b20d-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b20d-162">RELATED LINKS</span></span>

[<span data-ttu-id="1b20d-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b20d-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1b20d-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b20d-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="1b20d-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1b20d-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="1b20d-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1b20d-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
