---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: cee867b4597237a9593908a110aa3b46850437bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577240"
---
# <span data-ttu-id="698e5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="698e5-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="698e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="698e5-102">SYNOPSIS</span></span>
<span data-ttu-id="698e5-103">Hämtar information om en körnings tids nod.</span><span class="sxs-lookup"><span data-stu-id="698e5-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="698e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="698e5-104">SYNTAX</span></span>

### <span data-ttu-id="698e5-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="698e5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="698e5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="698e5-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="698e5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="698e5-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="698e5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="698e5-108">DESCRIPTION</span></span>
<span data-ttu-id="698e5-109">Cmdleten **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** hämtar detalj informationen för en integrations körnings nod.</span><span class="sxs-lookup"><span data-stu-id="698e5-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="698e5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="698e5-110">EXAMPLES</span></span>

### <span data-ttu-id="698e5-111">Exempel 1: hämtar detalj information om en integrations körnings nod.</span><span class="sxs-lookup"><span data-stu-id="698e5-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="698e5-112">Cmdleten hämtar information om noden "Node_1" i integrerings programmet "test-selfhost-IR" i Data Factory-DF-EU2.</span><span class="sxs-lookup"><span data-stu-id="698e5-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="698e5-113">Exempel 2: hämtar detalj information om en integrations-nod tillsammans med IP-adress.</span><span class="sxs-lookup"><span data-stu-id="698e5-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="698e5-114">Cmdleten får information om noden "Node_1" i integrerings programmet "test-selfhost-IR" i Data Factory ' test-DF-EU2 ', inklusive IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="698e5-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="698e5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="698e5-115">PARAMETERS</span></span>

### <span data-ttu-id="698e5-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="698e5-116">-DataFactoryName</span></span>
<span data-ttu-id="698e5-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="698e5-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698e5-118">-DefaultProfile</span></span>
<span data-ttu-id="698e5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="698e5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="698e5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="698e5-120">-InputObject</span></span>
<span data-ttu-id="698e5-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="698e5-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="698e5-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="698e5-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="698e5-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="698e5-124">-IpAddress</span></span>
<span data-ttu-id="698e5-125">IP-adressen för integration runtime-noden.</span><span class="sxs-lookup"><span data-stu-id="698e5-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="698e5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="698e5-126">-Name</span></span>
<span data-ttu-id="698e5-127">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="698e5-127">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="698e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="698e5-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="698e5-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="698e5-130">-ResourceId</span></span>
<span data-ttu-id="698e5-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="698e5-131">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698e5-132">CommonParameters</span></span>
<span data-ttu-id="698e5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698e5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698e5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698e5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="698e5-135">INPUTS</span></span>

### <span data-ttu-id="698e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="698e5-136">System.String</span></span>
<span data-ttu-id="698e5-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="698e5-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="698e5-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="698e5-138">OUTPUTS</span></span>

### <span data-ttu-id="698e5-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="698e5-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>
<span data-ttu-id="698e5-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="698e5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="698e5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="698e5-141">NOTES</span></span>
<span data-ttu-id="698e5-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="698e5-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="698e5-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="698e5-143">RELATED LINKS</span></span>

[<span data-ttu-id="698e5-144">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="698e5-144">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
