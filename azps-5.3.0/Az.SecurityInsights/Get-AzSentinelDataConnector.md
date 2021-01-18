---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525590"
---
# <span data-ttu-id="69504-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="69504-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="69504-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69504-102">SYNOPSIS</span></span>
<span data-ttu-id="69504-103">Skaffa en data koppling.</span><span class="sxs-lookup"><span data-stu-id="69504-103">Get a Data Connector.</span></span>

## <span data-ttu-id="69504-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69504-104">SYNTAX</span></span>

### <span data-ttu-id="69504-105">WorkspaceScope (standard)</span><span class="sxs-lookup"><span data-stu-id="69504-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69504-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="69504-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69504-107">ID</span><span class="sxs-lookup"><span data-stu-id="69504-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69504-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69504-108">DESCRIPTION</span></span>
<span data-ttu-id="69504-109">Cmdleten **Get-AzSentinelDataConnector** hämtar en data koppling från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="69504-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="69504-110">Om du anger parametern *DataConnectorId* returneras ett enskilt **DataConnector** -objekt.</span><span class="sxs-lookup"><span data-stu-id="69504-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="69504-111">Om du inte anger parametern *DataConnectorId* returneras en matris med alla data kopplingar på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="69504-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="69504-112">Du kan använda **DataConnector** -objektet för att uppdatera data anslutningen, till exempel om du vill inaktivera funktionen **DataConnector**.</span><span class="sxs-lookup"><span data-stu-id="69504-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="69504-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69504-113">EXAMPLES</span></span>

### <span data-ttu-id="69504-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69504-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="69504-115">Det här exemplet får alla **DataConnectors** på den angivna arbets ytan och lagrar dem sedan i $DataConnectors variabel.</span><span class="sxs-lookup"><span data-stu-id="69504-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="69504-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="69504-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="69504-117">Det här exemplet får en **DataConnector** på den angivna arbets ytan och lagrar den sedan i $DataConnector variabel.</span><span class="sxs-lookup"><span data-stu-id="69504-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="69504-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69504-118">PARAMETERS</span></span>

### <span data-ttu-id="69504-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="69504-119">-DataConnectorId</span></span>
<span data-ttu-id="69504-120">ID för data anslutning.</span><span class="sxs-lookup"><span data-stu-id="69504-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69504-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69504-121">-DefaultProfile</span></span>
<span data-ttu-id="69504-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69504-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69504-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69504-123">-ResourceGroupName</span></span>
<span data-ttu-id="69504-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="69504-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69504-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69504-125">-ResourceId</span></span>
<span data-ttu-id="69504-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="69504-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69504-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69504-127">-WorkspaceName</span></span>
<span data-ttu-id="69504-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="69504-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69504-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69504-129">CommonParameters</span></span>
<span data-ttu-id="69504-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69504-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69504-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69504-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69504-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69504-132">INPUTS</span></span>

### <span data-ttu-id="69504-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69504-133">System.String</span></span>
## <span data-ttu-id="69504-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69504-134">OUTPUTS</span></span>

### <span data-ttu-id="69504-135">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="69504-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="69504-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69504-136">NOTES</span></span>

## <span data-ttu-id="69504-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69504-137">RELATED LINKS</span></span>
