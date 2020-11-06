---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 9eb2b145f6a5968f460ba9a9506a4e0956793d01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574866"
---
# <span data-ttu-id="baaa1-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="baaa1-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="baaa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="baaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="baaa1-103">Uppdaterar en insikt i lagringen.</span><span class="sxs-lookup"><span data-stu-id="baaa1-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baaa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="baaa1-104">SYNTAX</span></span>

### <span data-ttu-id="baaa1-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="baaa1-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baaa1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="baaa1-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baaa1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="baaa1-107">DESCRIPTION</span></span>
<span data-ttu-id="baaa1-108">Cmdleten **set-AzureRmOperationalInsightsStorageInsight** ändrar konfigurationen för en inblick i lagringen.</span><span class="sxs-lookup"><span data-stu-id="baaa1-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="baaa1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="baaa1-109">EXAMPLES</span></span>

### <span data-ttu-id="baaa1-110">Exempel 1: ändra en data inblick efter namn</span><span class="sxs-lookup"><span data-stu-id="baaa1-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="baaa1-111">Det här kommandot ändrar de tabeller från vilka lagrings inblicken med namnet MyStorageInsight läser.</span><span class="sxs-lookup"><span data-stu-id="baaa1-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="baaa1-112">Exempel 2: ändra en inblick i lagringen med hjälp av ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="baaa1-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="baaa1-113">I det första kommandot används cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="baaa1-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="baaa1-114">Med det andra kommandot ändras de behållare från vilka lagrings inblicken med namnet MyStorageInsight läser.</span><span class="sxs-lookup"><span data-stu-id="baaa1-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="baaa1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="baaa1-115">PARAMETERS</span></span>

### <span data-ttu-id="baaa1-116">-Behållare</span><span class="sxs-lookup"><span data-stu-id="baaa1-116">-Containers</span></span>
<span data-ttu-id="baaa1-117">Anger listan med behållare som tillhandahåller data.</span><span class="sxs-lookup"><span data-stu-id="baaa1-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaa1-118">-DefaultProfile</span></span>
<span data-ttu-id="baaa1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="baaa1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="baaa1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="baaa1-120">-Name</span></span>
<span data-ttu-id="baaa1-121">Anger namnet på en inblick i lagringen.</span><span class="sxs-lookup"><span data-stu-id="baaa1-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baaa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="baaa1-123">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="baaa1-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="baaa1-124">-StorageAccountKey</span></span>
<span data-ttu-id="baaa1-125">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="baaa1-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-126">-Tabeller</span><span class="sxs-lookup"><span data-stu-id="baaa1-126">-Tables</span></span>
<span data-ttu-id="baaa1-127">Anger listan över tabeller som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="baaa1-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-128">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="baaa1-128">-Workspace</span></span>
<span data-ttu-id="baaa1-129">Anger arbets ytan som innehåller lagrings inblicken.</span><span class="sxs-lookup"><span data-stu-id="baaa1-129">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="baaa1-130">-WorkspaceName</span></span>
<span data-ttu-id="baaa1-131">Anger namnet på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="baaa1-131">Specifies the name of a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaa1-132">CommonParameters</span></span>
<span data-ttu-id="baaa1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baaa1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaa1-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaa1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaa1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="baaa1-135">INPUTS</span></span>

### <span data-ttu-id="baaa1-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="baaa1-136">PSWorkspace</span></span>
<span data-ttu-id="baaa1-137">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="baaa1-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="baaa1-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="baaa1-138">OUTPUTS</span></span>

### <span data-ttu-id="baaa1-139">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="baaa1-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="baaa1-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="baaa1-140">NOTES</span></span>

## <span data-ttu-id="baaa1-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="baaa1-141">RELATED LINKS</span></span>

[<span data-ttu-id="baaa1-142">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="baaa1-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="baaa1-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="baaa1-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


