---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919634"
---
# <span data-ttu-id="09f8f-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="09f8f-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="09f8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="09f8f-103">Hämta data källor under arbets ytan Azure logganalys Analytics.</span><span class="sxs-lookup"><span data-stu-id="09f8f-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="09f8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09f8f-104">SYNTAX</span></span>

### <span data-ttu-id="09f8f-105">ByWorkspaceNameByKind (standard)</span><span class="sxs-lookup"><span data-stu-id="09f8f-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f8f-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="09f8f-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f8f-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="09f8f-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f8f-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="09f8f-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f8f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09f8f-109">DESCRIPTION</span></span>
<span data-ttu-id="09f8f-110">Cmdleten **Get-AzOperationalInsightsDataSource** hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="09f8f-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="09f8f-111">Du kan ange en data källa att hämta.</span><span class="sxs-lookup"><span data-stu-id="09f8f-111">You can specify a data source to get.</span></span>
<span data-ttu-id="09f8f-112">Du kan filtrera resultaten baserat på typen av data källa.</span><span class="sxs-lookup"><span data-stu-id="09f8f-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="09f8f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09f8f-113">EXAMPLES</span></span>

## <span data-ttu-id="09f8f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09f8f-114">PARAMETERS</span></span>

### <span data-ttu-id="09f8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f8f-115">-DefaultProfile</span></span>
<span data-ttu-id="09f8f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="09f8f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09f8f-117">-Sort</span><span class="sxs-lookup"><span data-stu-id="09f8f-117">-Kind</span></span>
<span data-ttu-id="09f8f-118">Anger vilken typ av data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="09f8f-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="09f8f-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="09f8f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09f8f-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="09f8f-120">AzureActivityLog</span></span> 
- <span data-ttu-id="09f8f-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="09f8f-121">CustomLog</span></span> 
- <span data-ttu-id="09f8f-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="09f8f-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="09f8f-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="09f8f-123">LinuxSyslog</span></span> 
- <span data-ttu-id="09f8f-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="09f8f-124">WindowsEvent</span></span> 
- <span data-ttu-id="09f8f-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="09f8f-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f8f-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="09f8f-126">-Name</span></span>
<span data-ttu-id="09f8f-127">Anger namnet på en data källa som ska visas.</span><span class="sxs-lookup"><span data-stu-id="09f8f-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="09f8f-129">Anger namnet på en resurs grupp som innehåller data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="09f8f-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f8f-130">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="09f8f-130">-Workspace</span></span>
<span data-ttu-id="09f8f-131">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="09f8f-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09f8f-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09f8f-132">-WorkspaceName</span></span>
<span data-ttu-id="09f8f-133">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="09f8f-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f8f-134">CommonParameters</span></span>
<span data-ttu-id="09f8f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f8f-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f8f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f8f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09f8f-137">INPUTS</span></span>

### <span data-ttu-id="09f8f-138">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="09f8f-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="09f8f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="09f8f-139">System.String</span></span>

## <span data-ttu-id="09f8f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09f8f-140">OUTPUTS</span></span>

### <span data-ttu-id="09f8f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="09f8f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="09f8f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09f8f-142">NOTES</span></span>
* <span data-ttu-id="09f8f-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="09f8f-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="09f8f-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09f8f-144">RELATED LINKS</span></span>

[<span data-ttu-id="09f8f-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="09f8f-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="09f8f-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="09f8f-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)

