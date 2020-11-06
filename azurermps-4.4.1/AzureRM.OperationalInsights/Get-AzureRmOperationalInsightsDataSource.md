---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582279"
---
# <span data-ttu-id="64a5e-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="64a5e-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="64a5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="64a5e-103">Hämta data källor under arbets ytan Azure logganalys Analytics.</span><span class="sxs-lookup"><span data-stu-id="64a5e-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64a5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64a5e-104">SYNTAX</span></span>

### <span data-ttu-id="64a5e-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="64a5e-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a5e-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="64a5e-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a5e-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="64a5e-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a5e-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="64a5e-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a5e-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="64a5e-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64a5e-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64a5e-110">DESCRIPTION</span></span>
<span data-ttu-id="64a5e-111">Cmdleten **Get-AzureRmOperationalInsightsDataSource** hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="64a5e-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="64a5e-112">Du kan ange en data källa att hämta.</span><span class="sxs-lookup"><span data-stu-id="64a5e-112">You can specify a data source to get.</span></span>
<span data-ttu-id="64a5e-113">Du kan filtrera resultaten baserat på typen av data källa.</span><span class="sxs-lookup"><span data-stu-id="64a5e-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="64a5e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64a5e-114">EXAMPLES</span></span>

## <span data-ttu-id="64a5e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64a5e-115">PARAMETERS</span></span>

### <span data-ttu-id="64a5e-116">-Sort</span><span class="sxs-lookup"><span data-stu-id="64a5e-116">-Kind</span></span>
<span data-ttu-id="64a5e-117">Anger vilken typ av data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="64a5e-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="64a5e-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64a5e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64a5e-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="64a5e-119">AzureActivityLog</span></span> 
- <span data-ttu-id="64a5e-120">CustomLog</span><span class="sxs-lookup"><span data-stu-id="64a5e-120">CustomLog</span></span> 
- <span data-ttu-id="64a5e-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="64a5e-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="64a5e-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="64a5e-122">LinuxSyslog</span></span> 
- <span data-ttu-id="64a5e-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="64a5e-123">WindowsEvent</span></span> 
- <span data-ttu-id="64a5e-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="64a5e-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

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
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a5e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="64a5e-125">-Name</span></span>
<span data-ttu-id="64a5e-126">Anger namnet på en data källa som ska visas.</span><span class="sxs-lookup"><span data-stu-id="64a5e-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="64a5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="64a5e-128">Anger namnet på en resurs grupp som innehåller data källor som ska visas.</span><span class="sxs-lookup"><span data-stu-id="64a5e-128">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="64a5e-129">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="64a5e-129">-Workspace</span></span>
<span data-ttu-id="64a5e-130">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="64a5e-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="64a5e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64a5e-131">-WorkspaceName</span></span>
<span data-ttu-id="64a5e-132">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="64a5e-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="64a5e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a5e-133">-DefaultProfile</span></span>
<span data-ttu-id="64a5e-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64a5e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64a5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a5e-135">CommonParameters</span></span>
<span data-ttu-id="64a5e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a5e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a5e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a5e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64a5e-138">INPUTS</span></span>

### <span data-ttu-id="64a5e-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="64a5e-139">PSWorkspace</span></span>
<span data-ttu-id="64a5e-140">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="64a5e-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="64a5e-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="64a5e-141">PSWorkspace</span></span>
<span data-ttu-id="64a5e-142">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="64a5e-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="64a5e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64a5e-143">OUTPUTS</span></span>

### <span data-ttu-id="64a5e-144">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="64a5e-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="64a5e-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="64a5e-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="64a5e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64a5e-146">NOTES</span></span>
* <span data-ttu-id="64a5e-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="64a5e-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="64a5e-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64a5e-148">RELATED LINKS</span></span>

[<span data-ttu-id="64a5e-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="64a5e-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="64a5e-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="64a5e-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


