---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575174"
---
# <span data-ttu-id="72fe5-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72fe5-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="72fe5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="72fe5-103">Hämta data källor under arbets ytan Azure logganalys Analytics.</span><span class="sxs-lookup"><span data-stu-id="72fe5-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72fe5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72fe5-104">SYNTAX</span></span>

### <span data-ttu-id="72fe5-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="72fe5-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fe5-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="72fe5-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fe5-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="72fe5-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fe5-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="72fe5-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fe5-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="72fe5-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72fe5-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72fe5-110">DESCRIPTION</span></span>
<span data-ttu-id="72fe5-111">Cmdleten **Get-AzureRmOperationalInsightsDataSource** hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="72fe5-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="72fe5-112">Du kan ange en data källa att hämta.</span><span class="sxs-lookup"><span data-stu-id="72fe5-112">You can specify a data source to get.</span></span>
<span data-ttu-id="72fe5-113">Du kan filtrera resultaten baserat på typen av data källa.</span><span class="sxs-lookup"><span data-stu-id="72fe5-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="72fe5-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72fe5-114">EXAMPLES</span></span>

## <span data-ttu-id="72fe5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72fe5-115">PARAMETERS</span></span>

### <span data-ttu-id="72fe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fe5-116">-DefaultProfile</span></span>
<span data-ttu-id="72fe5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72fe5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72fe5-118">-Sort</span><span class="sxs-lookup"><span data-stu-id="72fe5-118">-Kind</span></span>
<span data-ttu-id="72fe5-119">Anger vilken typ av data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="72fe5-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="72fe5-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="72fe5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72fe5-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="72fe5-121">AzureActivityLog</span></span> 
- <span data-ttu-id="72fe5-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="72fe5-122">CustomLog</span></span> 
- <span data-ttu-id="72fe5-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="72fe5-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="72fe5-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="72fe5-124">LinuxSyslog</span></span> 
- <span data-ttu-id="72fe5-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="72fe5-125">WindowsEvent</span></span> 
- <span data-ttu-id="72fe5-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="72fe5-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fe5-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="72fe5-127">-Name</span></span>
<span data-ttu-id="72fe5-128">Anger namnet på en data källa som ska visas.</span><span class="sxs-lookup"><span data-stu-id="72fe5-128">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="72fe5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72fe5-129">-ResourceGroupName</span></span>
<span data-ttu-id="72fe5-130">Anger namnet på en resurs grupp som innehåller data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="72fe5-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fe5-131">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="72fe5-131">-Workspace</span></span>
<span data-ttu-id="72fe5-132">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="72fe5-132">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="72fe5-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72fe5-133">-WorkspaceName</span></span>
<span data-ttu-id="72fe5-134">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="72fe5-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72fe5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fe5-135">CommonParameters</span></span>
<span data-ttu-id="72fe5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fe5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fe5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fe5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fe5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72fe5-138">INPUTS</span></span>

### <span data-ttu-id="72fe5-139">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="72fe5-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="72fe5-140">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72fe5-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="72fe5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="72fe5-141">System.String</span></span>

## <span data-ttu-id="72fe5-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72fe5-142">OUTPUTS</span></span>

### <span data-ttu-id="72fe5-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="72fe5-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="72fe5-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72fe5-144">NOTES</span></span>
* <span data-ttu-id="72fe5-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="72fe5-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="72fe5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72fe5-146">RELATED LINKS</span></span>

[<span data-ttu-id="72fe5-147">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72fe5-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="72fe5-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72fe5-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


