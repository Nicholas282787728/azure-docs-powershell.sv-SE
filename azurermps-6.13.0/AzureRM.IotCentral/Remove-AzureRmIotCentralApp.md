---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585959"
---
# <span data-ttu-id="02535-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="02535-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="02535-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02535-102">SYNOPSIS</span></span>
<span data-ttu-id="02535-103">Tar bort ett IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="02535-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02535-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02535-104">SYNTAX</span></span>

### <span data-ttu-id="02535-105">ResourceIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02535-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02535-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02535-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02535-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="02535-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02535-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02535-108">DESCRIPTION</span></span>
<span data-ttu-id="02535-109">Tar bort ett befintligt IoT Central program.</span><span class="sxs-lookup"><span data-stu-id="02535-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="02535-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02535-110">EXAMPLES</span></span>

### <span data-ttu-id="02535-111">Exempel 1 Delete och IoT Central Application</span><span class="sxs-lookup"><span data-stu-id="02535-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="02535-112">Tar bort det tillhandahållna IoT Central-programmet.</span><span class="sxs-lookup"><span data-stu-id="02535-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="02535-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02535-113">PARAMETERS</span></span>

### <span data-ttu-id="02535-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02535-114">-AsJob</span></span>
<span data-ttu-id="02535-115">Kör cmdlet som ett jobb i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="02535-115">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02535-116">-DefaultProfile</span></span>
<span data-ttu-id="02535-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02535-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02535-118">-InputObject</span></span>
<span data-ttu-id="02535-119">IoT Central Application input-objekt.</span><span class="sxs-lookup"><span data-stu-id="02535-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02535-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="02535-120">-Name</span></span>
<span data-ttu-id="02535-121">Namnet på IoT Central program resursen.</span><span class="sxs-lookup"><span data-stu-id="02535-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02535-122">-PassThru</span></span>
<span data-ttu-id="02535-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="02535-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02535-124">-ResourceGroupName</span></span>
<span data-ttu-id="02535-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02535-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02535-126">-ResourceId</span></span>
<span data-ttu-id="02535-127">IoT Central program resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="02535-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02535-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02535-128">-Confirm</span></span>
<span data-ttu-id="02535-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02535-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02535-130">-WhatIf</span></span>
<span data-ttu-id="02535-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02535-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02535-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02535-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02535-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02535-133">CommonParameters</span></span>
<span data-ttu-id="02535-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02535-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02535-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02535-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02535-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02535-136">INPUTS</span></span>

### <span data-ttu-id="02535-137">System. String</span><span class="sxs-lookup"><span data-stu-id="02535-137">System.String</span></span>
### <span data-ttu-id="02535-138">Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="02535-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="02535-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02535-139">OUTPUTS</span></span>

### <span data-ttu-id="02535-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02535-140">System.Boolean</span></span>
## <span data-ttu-id="02535-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02535-141">NOTES</span></span>

## <span data-ttu-id="02535-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02535-142">RELATED LINKS</span></span>
