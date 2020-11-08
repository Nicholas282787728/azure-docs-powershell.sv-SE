---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271025"
---
# <span data-ttu-id="5e863-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5e863-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="5e863-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e863-102">SYNOPSIS</span></span>
<span data-ttu-id="5e863-103">Tar bort ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="5e863-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="5e863-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e863-104">SYNTAX</span></span>

### <span data-ttu-id="5e863-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5e863-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e863-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e863-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e863-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e863-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e863-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e863-108">DESCRIPTION</span></span>
<span data-ttu-id="5e863-109">Tar bort ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="5e863-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="5e863-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e863-110">EXAMPLES</span></span>

### <span data-ttu-id="5e863-111">Exempel 1 Delete och IoT Central Application</span><span class="sxs-lookup"><span data-stu-id="5e863-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="5e863-112">Tar bort det tillhandahållna IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="5e863-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="5e863-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e863-113">PARAMETERS</span></span>

### <span data-ttu-id="5e863-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e863-114">-AsJob</span></span>
<span data-ttu-id="5e863-115">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="5e863-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5e863-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e863-116">-DefaultProfile</span></span>
<span data-ttu-id="5e863-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e863-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e863-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e863-118">-InputObject</span></span>
<span data-ttu-id="5e863-119">IoT Central Application input-objekt.</span><span class="sxs-lookup"><span data-stu-id="5e863-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e863-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e863-120">-Name</span></span>
<span data-ttu-id="5e863-121">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="5e863-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e863-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e863-122">-PassThru</span></span>
<span data-ttu-id="5e863-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5e863-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5e863-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e863-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e863-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e863-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e863-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e863-126">-ResourceId</span></span>
<span data-ttu-id="5e863-127">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5e863-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e863-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e863-128">-Confirm</span></span>
<span data-ttu-id="5e863-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e863-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e863-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e863-130">-WhatIf</span></span>
<span data-ttu-id="5e863-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e863-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e863-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e863-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e863-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e863-133">CommonParameters</span></span>
<span data-ttu-id="5e863-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e863-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e863-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e863-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e863-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e863-136">INPUTS</span></span>

### <span data-ttu-id="5e863-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5e863-137">System.String</span></span>

### <span data-ttu-id="5e863-138">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5e863-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5e863-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e863-139">OUTPUTS</span></span>

### <span data-ttu-id="5e863-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e863-140">System.Boolean</span></span>

## <span data-ttu-id="5e863-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e863-141">NOTES</span></span>

## <span data-ttu-id="5e863-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e863-142">RELATED LINKS</span></span>
