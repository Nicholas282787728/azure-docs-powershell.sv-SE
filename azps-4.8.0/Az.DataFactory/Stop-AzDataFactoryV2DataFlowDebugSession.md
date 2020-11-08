---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260558"
---
# <span data-ttu-id="b8ff1-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b8ff1-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b8ff1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ff1-103">Stoppar en data flödes debug-session i Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="b8ff1-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="b8ff1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8ff1-104">SYNTAX</span></span>

### <span data-ttu-id="b8ff1-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8ff1-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8ff1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8ff1-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ff1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ff1-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8ff1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8ff1-108">DESCRIPTION</span></span>
<span data-ttu-id="b8ff1-109">Det här kommandot stoppar felsökningssessionen om den inte kommer att stängas av automatiskt enligt tids inställningen för Live-sessionen.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="b8ff1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8ff1-110">EXAMPLES</span></span>

### <span data-ttu-id="b8ff1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b8ff1-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="b8ff1-112">Stoppar en data flödes debug-session "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" i data fabriken "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="b8ff1-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="b8ff1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8ff1-113">PARAMETERS</span></span>

### <span data-ttu-id="b8ff1-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8ff1-114">-DataFactory</span></span>
<span data-ttu-id="b8ff1-115">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-115">The data factory object.</span></span>

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

### <span data-ttu-id="b8ff1-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8ff1-116">-DataFactoryName</span></span>
<span data-ttu-id="b8ff1-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-117">The data factory name.</span></span>

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

### <span data-ttu-id="b8ff1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ff1-118">-DefaultProfile</span></span>
<span data-ttu-id="b8ff1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ff1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8ff1-120">-PassThru</span></span>
<span data-ttu-id="b8ff1-121">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b8ff1-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8ff1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ff1-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8ff1-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-124">The resource group name.</span></span>

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

### <span data-ttu-id="b8ff1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ff1-125">-ResourceId</span></span>
<span data-ttu-id="b8ff1-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b8ff1-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="b8ff1-127">-SessionId</span></span>
<span data-ttu-id="b8ff1-128">ID för debug-session med data flöde.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ff1-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8ff1-129">-Confirm</span></span>
<span data-ttu-id="b8ff1-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ff1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ff1-131">-WhatIf</span></span>
<span data-ttu-id="b8ff1-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8ff1-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ff1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ff1-134">CommonParameters</span></span>
<span data-ttu-id="b8ff1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ff1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ff1-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ff1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ff1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8ff1-137">INPUTS</span></span>

### <span data-ttu-id="b8ff1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ff1-138">System.String</span></span>

### <span data-ttu-id="b8ff1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b8ff1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b8ff1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8ff1-140">OUTPUTS</span></span>

### <span data-ttu-id="b8ff1-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="b8ff1-141">System.Void</span></span>

### <span data-ttu-id="b8ff1-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8ff1-142">System.Boolean</span></span>

## <span data-ttu-id="b8ff1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8ff1-143">NOTES</span></span>
<span data-ttu-id="b8ff1-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b8ff1-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8ff1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8ff1-145">RELATED LINKS</span></span>

[<span data-ttu-id="b8ff1-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b8ff1-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b8ff1-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b8ff1-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b8ff1-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b8ff1-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="b8ff1-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="b8ff1-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)