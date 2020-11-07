---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 6905e16667fd2a4378474950d928ef730ed1786e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744034"
---
# <span data-ttu-id="f22cb-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f22cb-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="f22cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f22cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f22cb-103">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="f22cb-103">Deletes a service instance.</span></span>

## <span data-ttu-id="f22cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f22cb-104">SYNTAX</span></span>

### <span data-ttu-id="f22cb-105">ServiceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f22cb-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22cb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22cb-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22cb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f22cb-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f22cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f22cb-108">DESCRIPTION</span></span>
<span data-ttu-id="f22cb-109">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="f22cb-109">Deletes a service instance.</span></span>

## <span data-ttu-id="f22cb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f22cb-110">EXAMPLES</span></span>

### <span data-ttu-id="f22cb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f22cb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="f22cb-112">Tar bort den befintliga HealthcareApis-tjänsten med det medföljande namnet i en tillhandahållen resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f22cb-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="f22cb-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f22cb-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="f22cb-114">Tar bort den befintliga HealthcareApis-tjänsten med angiven ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f22cb-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="f22cb-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f22cb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="f22cb-116">Tar bort det tillhandahållna HealthcareApis-serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="f22cb-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="f22cb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f22cb-117">PARAMETERS</span></span>

### <span data-ttu-id="f22cb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f22cb-118">-AsJob</span></span>
<span data-ttu-id="f22cb-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="f22cb-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f22cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22cb-120">-DefaultProfile</span></span>
<span data-ttu-id="f22cb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f22cb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22cb-122">-InputObject</span></span>
<span data-ttu-id="f22cb-123">HealthcareApis-tjänst objekt</span><span class="sxs-lookup"><span data-stu-id="f22cb-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="f22cb-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f22cb-124">-Name</span></span>
<span data-ttu-id="f22cb-125">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="f22cb-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="f22cb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f22cb-126">-PassThru</span></span>
<span data-ttu-id="f22cb-127">Returnerar sant om åtgärden lyckades</span><span class="sxs-lookup"><span data-stu-id="f22cb-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="f22cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="f22cb-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f22cb-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f22cb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22cb-130">-ResourceId</span></span>
<span data-ttu-id="f22cb-131">HealthcareApis-tjänst ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f22cb-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="f22cb-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f22cb-132">-Confirm</span></span>
<span data-ttu-id="f22cb-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f22cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22cb-134">-WhatIf</span></span>
<span data-ttu-id="f22cb-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f22cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22cb-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f22cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22cb-137">CommonParameters</span></span>
<span data-ttu-id="f22cb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22cb-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f22cb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22cb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f22cb-140">INPUTS</span></span>

### <span data-ttu-id="f22cb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f22cb-141">System.String</span></span>

### <span data-ttu-id="f22cb-142">Microsoft. Azure. commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f22cb-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="f22cb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f22cb-143">OUTPUTS</span></span>

### <span data-ttu-id="f22cb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f22cb-144">System.Boolean</span></span>

## <span data-ttu-id="f22cb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f22cb-145">NOTES</span></span>

## <span data-ttu-id="f22cb-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f22cb-146">RELATED LINKS</span></span>