---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b81d7e7d87e8db7658db425f889630a3897d1ecd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755046"
---
# <span data-ttu-id="d2a4d-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d2a4d-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="d2a4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a4d-103">Uppdaterar en insikt i lagringen.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="d2a4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2a4d-104">SYNTAX</span></span>

### <span data-ttu-id="d2a4d-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="d2a4d-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2a4d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2a4d-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2a4d-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a4d-108">Cmdleten **set-AzOperationalInsightsStorageInsight** ändrar konfigurationen för en inblick i lagringen.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="d2a4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2a4d-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a4d-110">Exempel 1: ändra en data inblick efter namn</span><span class="sxs-lookup"><span data-stu-id="d2a4d-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="d2a4d-111">Det här kommandot ändrar de tabeller från vilka lagrings inblicken med namnet MyStorageInsight läser.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="d2a4d-112">Exempel 2: ändra en inblick i lagringen med hjälp av ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="d2a4d-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="d2a4d-113">I det första kommandot används cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="d2a4d-114">Med det andra kommandot ändras de behållare från vilka lagrings inblicken med namnet MyStorageInsight läser.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="d2a4d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2a4d-115">PARAMETERS</span></span>

### <span data-ttu-id="d2a4d-116">-Behållare</span><span class="sxs-lookup"><span data-stu-id="d2a4d-116">-Containers</span></span>
<span data-ttu-id="d2a4d-117">Anger listan med behållare som tillhandahåller data.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a4d-118">-DefaultProfile</span></span>
<span data-ttu-id="d2a4d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d2a4d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2a4d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2a4d-120">-Name</span></span>
<span data-ttu-id="d2a4d-121">Anger namnet på en inblick i lagringen.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2a4d-123">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d2a4d-124">-StorageAccountKey</span></span>
<span data-ttu-id="d2a4d-125">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-126">-Tabeller</span><span class="sxs-lookup"><span data-stu-id="d2a4d-126">-Tables</span></span>
<span data-ttu-id="d2a4d-127">Anger listan över tabeller som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-128">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="d2a4d-128">-Workspace</span></span>
<span data-ttu-id="d2a4d-129">Anger arbets ytan som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-129">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2a4d-130">-WorkspaceName</span></span>
<span data-ttu-id="d2a4d-131">Anger namnet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-131">Specifies the name of a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2a4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a4d-132">CommonParameters</span></span>
<span data-ttu-id="d2a4d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a4d-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a4d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a4d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2a4d-135">INPUTS</span></span>

### <span data-ttu-id="d2a4d-136">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2a4d-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d2a4d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a4d-137">System.String</span></span>

### <span data-ttu-id="d2a4d-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="d2a4d-138">System.String[]</span></span>

## <span data-ttu-id="d2a4d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2a4d-139">OUTPUTS</span></span>

### <span data-ttu-id="d2a4d-140">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d2a4d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="d2a4d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2a4d-141">NOTES</span></span>

## <span data-ttu-id="d2a4d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2a4d-142">RELATED LINKS</span></span>

[<span data-ttu-id="d2a4d-143">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="d2a4d-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="d2a4d-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2a4d-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

