---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391120"
---
# <span data-ttu-id="52798-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="52798-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="52798-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52798-102">SYNOPSIS</span></span>
<span data-ttu-id="52798-103">Visar en lista över alla eller en särskild IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="52798-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="52798-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52798-104">SYNTAX</span></span>

### <span data-ttu-id="52798-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52798-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52798-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52798-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52798-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="52798-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52798-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52798-108">DESCRIPTION</span></span>
<span data-ttu-id="52798-109">Få information om en IoT Edge-distribution eller lista IoT Edge-installationer i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="52798-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="52798-110">Mer https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring information finns i.</span><span class="sxs-lookup"><span data-stu-id="52798-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="52798-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52798-111">EXAMPLES</span></span>

### <span data-ttu-id="52798-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52798-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="52798-113">Få information om en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="52798-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="52798-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52798-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="52798-115">Lista alla IoT Edge-installationer i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="52798-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="52798-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52798-116">PARAMETERS</span></span>

### <span data-ttu-id="52798-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52798-117">-DefaultProfile</span></span>
<span data-ttu-id="52798-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52798-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52798-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52798-119">-InputObject</span></span>
<span data-ttu-id="52798-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="52798-120">IotHub object</span></span>

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

### <span data-ttu-id="52798-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="52798-121">-IotHubName</span></span>
<span data-ttu-id="52798-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="52798-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="52798-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="52798-123">-Name</span></span>
<span data-ttu-id="52798-124">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="52798-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="52798-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52798-125">-ResourceGroupName</span></span>
<span data-ttu-id="52798-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="52798-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="52798-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52798-127">-ResourceId</span></span>
<span data-ttu-id="52798-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="52798-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="52798-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52798-129">CommonParameters</span></span>
<span data-ttu-id="52798-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52798-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52798-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52798-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52798-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52798-132">INPUTS</span></span>

### <span data-ttu-id="52798-133">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="52798-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="52798-134">System. String</span><span class="sxs-lookup"><span data-stu-id="52798-134">System.String</span></span>

## <span data-ttu-id="52798-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52798-135">OUTPUTS</span></span>

### <span data-ttu-id="52798-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="52798-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="52798-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="52798-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="52798-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52798-138">NOTES</span></span>

## <span data-ttu-id="52798-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52798-139">RELATED LINKS</span></span>
