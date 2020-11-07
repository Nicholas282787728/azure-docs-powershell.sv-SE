---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 1521f0f4f3b90010e24185a036dca047860e27c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744789"
---
# <span data-ttu-id="fd014-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fd014-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="fd014-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd014-102">SYNOPSIS</span></span>
<span data-ttu-id="fd014-103">Få alla aktiva data flödes debug-sessioner av Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="fd014-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="fd014-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd014-104">SYNTAX</span></span>

### <span data-ttu-id="fd014-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="fd014-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd014-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd014-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd014-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fd014-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd014-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd014-108">DESCRIPTION</span></span>
<span data-ttu-id="fd014-109">Lista alla aktiva data flödes debug-sessioner av Azure Data Factory med uppgifter.</span><span class="sxs-lookup"><span data-stu-id="fd014-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="fd014-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd014-110">EXAMPLES</span></span>

### <span data-ttu-id="fd014-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd014-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="fd014-112">Hämta alla aktiva data flödes-sessioner i Azure Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="fd014-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="fd014-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd014-113">PARAMETERS</span></span>

### <span data-ttu-id="fd014-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fd014-114">-DataFactory</span></span>
<span data-ttu-id="fd014-115">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="fd014-115">The data factory object.</span></span>

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

### <span data-ttu-id="fd014-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fd014-116">-DataFactoryName</span></span>
<span data-ttu-id="fd014-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fd014-117">The data factory name.</span></span>

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

### <span data-ttu-id="fd014-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd014-118">-DefaultProfile</span></span>
<span data-ttu-id="fd014-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd014-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd014-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd014-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd014-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fd014-121">The resource group name.</span></span>

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

### <span data-ttu-id="fd014-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd014-122">-ResourceId</span></span>
<span data-ttu-id="fd014-123">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="fd014-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fd014-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd014-124">CommonParameters</span></span>
<span data-ttu-id="fd014-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd014-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd014-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd014-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd014-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd014-127">INPUTS</span></span>

### <span data-ttu-id="fd014-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fd014-128">System.String</span></span>

### <span data-ttu-id="fd014-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fd014-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fd014-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd014-130">OUTPUTS</span></span>

### <span data-ttu-id="fd014-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="fd014-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="fd014-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd014-132">NOTES</span></span>
<span data-ttu-id="fd014-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="fd014-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fd014-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd014-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd014-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fd014-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="fd014-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="fd014-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="fd014-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="fd014-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="fd014-138">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fd014-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)