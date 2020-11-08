---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270607"
---
# <span data-ttu-id="cacff-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cacff-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="cacff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cacff-102">SYNOPSIS</span></span>
<span data-ttu-id="cacff-103">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="cacff-103">Deletes a service instance.</span></span>

## <span data-ttu-id="cacff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cacff-104">SYNTAX</span></span>

### <span data-ttu-id="cacff-105">ServiceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cacff-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cacff-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cacff-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cacff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cacff-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cacff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cacff-108">DESCRIPTION</span></span>
<span data-ttu-id="cacff-109">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="cacff-109">Deletes a service instance.</span></span>

## <span data-ttu-id="cacff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cacff-110">EXAMPLES</span></span>

### <span data-ttu-id="cacff-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cacff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="cacff-112">Tar bort den befintliga HealthcareApis-tjänsten med det medföljande namnet i en tillhandahållen resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cacff-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="cacff-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cacff-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="cacff-114">Tar bort den befintliga HealthcareApis-tjänsten med angiven ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cacff-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="cacff-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="cacff-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="cacff-116">Tar bort det tillhandahållna HealthcareApis-serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="cacff-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="cacff-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cacff-117">PARAMETERS</span></span>

### <span data-ttu-id="cacff-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cacff-118">-AsJob</span></span>
<span data-ttu-id="cacff-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="cacff-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="cacff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacff-120">-DefaultProfile</span></span>
<span data-ttu-id="cacff-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cacff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cacff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cacff-122">-InputObject</span></span>
<span data-ttu-id="cacff-123">HealthcareApis-tjänst objekt</span><span class="sxs-lookup"><span data-stu-id="cacff-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="cacff-124">-Name</span></span>
<span data-ttu-id="cacff-125">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="cacff-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cacff-126">-PassThru</span></span>
<span data-ttu-id="cacff-127">Returnerar sant om åtgärden lyckades</span><span class="sxs-lookup"><span data-stu-id="cacff-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="cacff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cacff-128">-ResourceGroupName</span></span>
<span data-ttu-id="cacff-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cacff-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cacff-130">-ResourceId</span></span>
<span data-ttu-id="cacff-131">HealthcareApis-tjänst ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cacff-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacff-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cacff-132">-Confirm</span></span>
<span data-ttu-id="cacff-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cacff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cacff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cacff-134">-WhatIf</span></span>
<span data-ttu-id="cacff-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cacff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cacff-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cacff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cacff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacff-137">CommonParameters</span></span>
<span data-ttu-id="cacff-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacff-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cacff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacff-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cacff-140">INPUTS</span></span>

### <span data-ttu-id="cacff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cacff-141">System.String</span></span>

### <span data-ttu-id="cacff-142">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cacff-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="cacff-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cacff-143">OUTPUTS</span></span>

### <span data-ttu-id="cacff-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cacff-144">System.Boolean</span></span>

## <span data-ttu-id="cacff-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cacff-145">NOTES</span></span>

## <span data-ttu-id="cacff-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cacff-146">RELATED LINKS</span></span>
