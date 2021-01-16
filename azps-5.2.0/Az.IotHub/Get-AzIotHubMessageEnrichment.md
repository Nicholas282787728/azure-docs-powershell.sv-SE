---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409963"
---
# <span data-ttu-id="f800e-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f800e-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f800e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f800e-102">SYNOPSIS</span></span>
<span data-ttu-id="f800e-103">Visar en lista över alla meddelanden eller ett visst meddelande för IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="f800e-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="f800e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f800e-104">SYNTAX</span></span>

### <span data-ttu-id="f800e-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f800e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f800e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f800e-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f800e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f800e-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f800e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f800e-108">DESCRIPTION</span></span>
<span data-ttu-id="f800e-109">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f800e-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f800e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f800e-110">EXAMPLES</span></span>

### <span data-ttu-id="f800e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f800e-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="f800e-112">Lista alla meddelanden som berikas i MyIotHub</span><span class="sxs-lookup"><span data-stu-id="f800e-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="f800e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f800e-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="f800e-114">Visa information om meddelandet "newKey".</span><span class="sxs-lookup"><span data-stu-id="f800e-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="f800e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f800e-115">PARAMETERS</span></span>

### <span data-ttu-id="f800e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f800e-116">-DefaultProfile</span></span>
<span data-ttu-id="f800e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f800e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f800e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f800e-118">-InputObject</span></span>
<span data-ttu-id="f800e-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="f800e-119">IotHub object</span></span>

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

### <span data-ttu-id="f800e-120">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="f800e-120">-Key</span></span>
<span data-ttu-id="f800e-121">Beriknings tangenten.</span><span class="sxs-lookup"><span data-stu-id="f800e-121">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f800e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f800e-122">-Name</span></span>
<span data-ttu-id="f800e-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="f800e-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f800e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f800e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f800e-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f800e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f800e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f800e-126">-ResourceId</span></span>
<span data-ttu-id="f800e-127">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="f800e-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f800e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f800e-128">CommonParameters</span></span>
<span data-ttu-id="f800e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f800e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f800e-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f800e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f800e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f800e-131">INPUTS</span></span>

### <span data-ttu-id="f800e-132">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f800e-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f800e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f800e-133">System.String</span></span>

## <span data-ttu-id="f800e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f800e-134">OUTPUTS</span></span>

### <span data-ttu-id="f800e-135">Microsoft. Azure. commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f800e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="f800e-136">Microsoft. Azure. commands. Management. IotHub. Models. PSEnrichmentProperties []</span><span class="sxs-lookup"><span data-stu-id="f800e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="f800e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f800e-137">NOTES</span></span>

## <span data-ttu-id="f800e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f800e-138">RELATED LINKS</span></span>
