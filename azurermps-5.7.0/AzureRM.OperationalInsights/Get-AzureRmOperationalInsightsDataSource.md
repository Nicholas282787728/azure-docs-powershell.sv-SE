---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577108"
---
# <span data-ttu-id="99b33-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="99b33-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="99b33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99b33-102">SYNOPSIS</span></span>
<span data-ttu-id="99b33-103">Hämta data källor under arbets ytan Azure logganalys Analytics.</span><span class="sxs-lookup"><span data-stu-id="99b33-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99b33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99b33-104">SYNTAX</span></span>

### <span data-ttu-id="99b33-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="99b33-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b33-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="99b33-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b33-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="99b33-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b33-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="99b33-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b33-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="99b33-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b33-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99b33-110">DESCRIPTION</span></span>
<span data-ttu-id="99b33-111">Cmdleten **Get-AzureRmOperationalInsightsDataSource** hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="99b33-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="99b33-112">Du kan ange en data källa att hämta.</span><span class="sxs-lookup"><span data-stu-id="99b33-112">You can specify a data source to get.</span></span>
<span data-ttu-id="99b33-113">Du kan filtrera resultaten baserat på typen av data källa.</span><span class="sxs-lookup"><span data-stu-id="99b33-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="99b33-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99b33-114">EXAMPLES</span></span>

## <span data-ttu-id="99b33-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99b33-115">PARAMETERS</span></span>

### <span data-ttu-id="99b33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b33-116">-DefaultProfile</span></span>
<span data-ttu-id="99b33-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99b33-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99b33-118">-Sort</span><span class="sxs-lookup"><span data-stu-id="99b33-118">-Kind</span></span>
<span data-ttu-id="99b33-119">Anger vilken typ av data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="99b33-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="99b33-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="99b33-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99b33-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="99b33-121">AzureActivityLog</span></span> 
- <span data-ttu-id="99b33-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="99b33-122">CustomLog</span></span> 
- <span data-ttu-id="99b33-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="99b33-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="99b33-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="99b33-124">LinuxSyslog</span></span> 
- <span data-ttu-id="99b33-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="99b33-125">WindowsEvent</span></span> 
- <span data-ttu-id="99b33-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="99b33-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
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
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b33-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="99b33-127">-Name</span></span>
<span data-ttu-id="99b33-128">Anger namnet på en data källa som ska visas.</span><span class="sxs-lookup"><span data-stu-id="99b33-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b33-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b33-129">-ResourceGroupName</span></span>
<span data-ttu-id="99b33-130">Anger namnet på en resurs grupp som innehåller data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="99b33-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b33-131">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="99b33-131">-Workspace</span></span>
<span data-ttu-id="99b33-132">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="99b33-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b33-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99b33-133">-WorkspaceName</span></span>
<span data-ttu-id="99b33-134">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="99b33-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b33-135">CommonParameters</span></span>
<span data-ttu-id="99b33-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b33-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b33-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b33-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99b33-138">INPUTS</span></span>

### <span data-ttu-id="99b33-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="99b33-139">PSWorkspace</span></span>
<span data-ttu-id="99b33-140">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99b33-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="99b33-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="99b33-141">PSWorkspace</span></span>
<span data-ttu-id="99b33-142">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99b33-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="99b33-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99b33-143">OUTPUTS</span></span>

### <span data-ttu-id="99b33-144">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="99b33-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="99b33-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="99b33-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="99b33-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99b33-146">NOTES</span></span>
* <span data-ttu-id="99b33-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="99b33-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="99b33-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99b33-148">RELATED LINKS</span></span>

[<span data-ttu-id="99b33-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="99b33-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="99b33-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="99b33-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


