---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 602ad3506f4a4fc0f8aa22128ca223e6a90f6ab5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415795"
---
# <span data-ttu-id="85554-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="85554-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="85554-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85554-102">SYNOPSIS</span></span>
<span data-ttu-id="85554-103">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="85554-103">Deletes a service instance.</span></span>

## <span data-ttu-id="85554-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85554-104">SYNTAX</span></span>

### <span data-ttu-id="85554-105">ServiceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85554-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85554-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85554-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85554-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85554-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85554-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85554-108">DESCRIPTION</span></span>
<span data-ttu-id="85554-109">Tar bort en tjänst instans.</span><span class="sxs-lookup"><span data-stu-id="85554-109">Deletes a service instance.</span></span>

## <span data-ttu-id="85554-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85554-110">EXAMPLES</span></span>

### <span data-ttu-id="85554-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85554-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="85554-112">Tar bort den befintliga HealthcareApis-tjänsten med det medföljande namnet i en tillhandahållen resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="85554-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="85554-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="85554-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="85554-114">Tar bort den befintliga HealthcareApis-tjänsten med angiven ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85554-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="85554-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="85554-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="85554-116">Tar bort det tillhandahållna HealthcareApis-serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="85554-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="85554-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85554-117">PARAMETERS</span></span>

### <span data-ttu-id="85554-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85554-118">-AsJob</span></span>
<span data-ttu-id="85554-119">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="85554-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="85554-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85554-120">-DefaultProfile</span></span>
<span data-ttu-id="85554-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85554-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85554-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85554-122">-InputObject</span></span>
<span data-ttu-id="85554-123">HealthcareApis-tjänst objekt</span><span class="sxs-lookup"><span data-stu-id="85554-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="85554-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="85554-124">-Name</span></span>
<span data-ttu-id="85554-125">HealthcareApis-tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="85554-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="85554-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85554-126">-PassThru</span></span>
<span data-ttu-id="85554-127">Returnerar sant om åtgärden lyckades</span><span class="sxs-lookup"><span data-stu-id="85554-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="85554-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85554-128">-ResourceGroupName</span></span>
<span data-ttu-id="85554-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="85554-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="85554-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85554-130">-ResourceId</span></span>
<span data-ttu-id="85554-131">HealthcareApis-tjänst ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85554-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="85554-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85554-132">-Confirm</span></span>
<span data-ttu-id="85554-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85554-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85554-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85554-134">-WhatIf</span></span>
<span data-ttu-id="85554-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85554-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85554-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85554-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85554-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85554-137">CommonParameters</span></span>
<span data-ttu-id="85554-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85554-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85554-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85554-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85554-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85554-140">INPUTS</span></span>

### <span data-ttu-id="85554-141">Microsoft. Azure. commands. HealthcareApis. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="85554-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="85554-142">System. String</span><span class="sxs-lookup"><span data-stu-id="85554-142">System.String</span></span>

## <span data-ttu-id="85554-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85554-143">OUTPUTS</span></span>

### <span data-ttu-id="85554-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85554-144">System.Boolean</span></span>

## <span data-ttu-id="85554-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85554-145">NOTES</span></span>

## <span data-ttu-id="85554-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85554-146">RELATED LINKS</span></span>
