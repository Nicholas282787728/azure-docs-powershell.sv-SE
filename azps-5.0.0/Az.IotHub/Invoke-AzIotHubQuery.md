---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273485"
---
# <span data-ttu-id="62755-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="62755-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="62755-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62755-102">SYNOPSIS</span></span>
<span data-ttu-id="62755-103">Fråga en IoT-hubb med ett kraftfullt SQL-gilla-språk.</span><span class="sxs-lookup"><span data-stu-id="62755-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="62755-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62755-104">SYNTAX</span></span>

### <span data-ttu-id="62755-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="62755-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62755-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62755-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62755-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62755-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62755-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62755-108">DESCRIPTION</span></span>
<span data-ttu-id="62755-109">Fråga en IoT-hubb med ett kraftfullt SQL-liknande språk för att hämta information om enheter och moduler till en och samma jobb och meddelanderoutning.</span><span class="sxs-lookup"><span data-stu-id="62755-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="62755-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language information finns i.</span><span class="sxs-lookup"><span data-stu-id="62755-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="62755-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62755-111">EXAMPLES</span></span>

### <span data-ttu-id="62755-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62755-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="62755-113">Fråga alla enheter med dubbla data i ett Azure IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="62755-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="62755-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="62755-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="62755-115">Fråga Top 2-modul med dubbla data på en målen het.</span><span class="sxs-lookup"><span data-stu-id="62755-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="62755-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62755-116">PARAMETERS</span></span>

### <span data-ttu-id="62755-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62755-117">-DefaultProfile</span></span>
<span data-ttu-id="62755-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62755-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62755-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62755-119">-InputObject</span></span>
<span data-ttu-id="62755-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="62755-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62755-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62755-121">-IotHubName</span></span>
<span data-ttu-id="62755-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="62755-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62755-123">-Fråga</span><span class="sxs-lookup"><span data-stu-id="62755-123">-Query</span></span>
<span data-ttu-id="62755-124">Användar fråga som ska utföras.</span><span class="sxs-lookup"><span data-stu-id="62755-124">User query to be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62755-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62755-125">-ResourceGroupName</span></span>
<span data-ttu-id="62755-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="62755-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62755-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62755-127">-ResourceId</span></span>
<span data-ttu-id="62755-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="62755-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62755-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="62755-129">-Top</span></span>
<span data-ttu-id="62755-130">Maximalt antal element som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="62755-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="62755-131">Som standard har frågan inget Cap.</span><span class="sxs-lookup"><span data-stu-id="62755-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62755-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62755-132">-Confirm</span></span>
<span data-ttu-id="62755-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62755-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62755-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62755-134">-WhatIf</span></span>
<span data-ttu-id="62755-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62755-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62755-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62755-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62755-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62755-137">CommonParameters</span></span>
<span data-ttu-id="62755-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62755-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62755-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62755-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62755-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62755-140">INPUTS</span></span>

### <span data-ttu-id="62755-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62755-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62755-142">System. String</span><span class="sxs-lookup"><span data-stu-id="62755-142">System.String</span></span>

## <span data-ttu-id="62755-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62755-143">OUTPUTS</span></span>

### <span data-ttu-id="62755-144">System. String</span><span class="sxs-lookup"><span data-stu-id="62755-144">System.String</span></span>

## <span data-ttu-id="62755-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62755-145">NOTES</span></span>

## <span data-ttu-id="62755-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62755-146">RELATED LINKS</span></span>
