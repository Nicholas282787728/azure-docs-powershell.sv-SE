---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102943"
---
# <span data-ttu-id="6424c-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6424c-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="6424c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6424c-102">SYNOPSIS</span></span>
<span data-ttu-id="6424c-103">Få alla aktiva data flödes debug-sessioner av Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="6424c-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="6424c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6424c-104">SYNTAX</span></span>

### <span data-ttu-id="6424c-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="6424c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6424c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6424c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6424c-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6424c-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6424c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6424c-108">DESCRIPTION</span></span>
<span data-ttu-id="6424c-109">Lista alla aktiva data flödes debug-sessioner av Azure Data Factory med uppgifter.</span><span class="sxs-lookup"><span data-stu-id="6424c-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="6424c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6424c-110">EXAMPLES</span></span>

### <span data-ttu-id="6424c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6424c-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="6424c-112">Hämta alla aktiva data flödes-sessioner i Azure Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6424c-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="6424c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6424c-113">PARAMETERS</span></span>

### <span data-ttu-id="6424c-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6424c-114">-DataFactory</span></span>
<span data-ttu-id="6424c-115">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="6424c-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6424c-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6424c-116">-DataFactoryName</span></span>
<span data-ttu-id="6424c-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="6424c-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6424c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6424c-118">-DefaultProfile</span></span>
<span data-ttu-id="6424c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6424c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6424c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6424c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6424c-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6424c-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6424c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6424c-122">-ResourceId</span></span>
<span data-ttu-id="6424c-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="6424c-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6424c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6424c-124">CommonParameters</span></span>
<span data-ttu-id="6424c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6424c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6424c-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6424c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6424c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6424c-127">INPUTS</span></span>

### <span data-ttu-id="6424c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6424c-128">System.String</span></span>

### <span data-ttu-id="6424c-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6424c-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6424c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6424c-130">OUTPUTS</span></span>

### <span data-ttu-id="6424c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="6424c-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="6424c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6424c-132">NOTES</span></span>
<span data-ttu-id="6424c-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="6424c-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6424c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6424c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6424c-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6424c-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="6424c-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="6424c-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="6424c-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="6424c-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="6424c-138">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6424c-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)