---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584220"
---
# <span data-ttu-id="9d9d8-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="9d9d8-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="9d9d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9d8-103">Uppdatera en Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d9d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d9d8-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9d8-106">Du kan uppdatera egenskaperna för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="9d9d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d9d8-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9d8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9d9d8-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="9d9d8-109">Lägg till " @tags " i taggen för en Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="9d9d8-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="9d9d8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d9d8-110">PARAMETERS</span></span>

### <span data-ttu-id="9d9d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9d8-111">-DefaultProfile</span></span>
<span data-ttu-id="9d9d8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9d8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d9d8-113">-Name</span></span>
<span data-ttu-id="9d9d8-114">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9d9d8-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9d9d8-115">-Återställ</span><span class="sxs-lookup"><span data-stu-id="9d9d8-115">-Reset</span></span>
<span data-ttu-id="9d9d8-116">Återställa IoTHub-Taggar</span><span class="sxs-lookup"><span data-stu-id="9d9d8-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="9d9d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d9d8-118">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9d9d8-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9d9d8-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9d9d8-119">-Tag</span></span>
<span data-ttu-id="9d9d8-120">IoTHub agg</span><span class="sxs-lookup"><span data-stu-id="9d9d8-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9d8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d9d8-121">-Confirm</span></span>
<span data-ttu-id="9d9d8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9d8-123">-WhatIf</span></span>
<span data-ttu-id="9d9d8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9d8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9d8-126">CommonParameters</span></span>
<span data-ttu-id="9d9d8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9d8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9d8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d9d8-129">INPUTS</span></span>

### <span data-ttu-id="9d9d8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9d9d8-130">System.String</span></span>

## <span data-ttu-id="9d9d8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d9d8-131">OUTPUTS</span></span>

### <span data-ttu-id="9d9d8-132">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9d9d8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9d9d8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d9d8-133">NOTES</span></span>

## <span data-ttu-id="9d9d8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d9d8-134">RELATED LINKS</span></span>
