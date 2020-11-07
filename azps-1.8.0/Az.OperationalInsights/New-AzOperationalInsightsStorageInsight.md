---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e4f966d542110f96672857c2222d44ae03d331ba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928522"
---
# <span data-ttu-id="c4440-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c4440-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="c4440-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4440-102">SYNOPSIS</span></span>
<span data-ttu-id="c4440-103">Skapar en inblick i en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c4440-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="c4440-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4440-104">SYNTAX</span></span>

### <span data-ttu-id="c4440-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c4440-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4440-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c4440-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4440-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4440-107">DESCRIPTION</span></span>
<span data-ttu-id="c4440-108">**New-AzOperationalInsightsStorageInsight-** cmdleten skapar en ny inblick i en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c4440-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="c4440-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4440-109">EXAMPLES</span></span>

### <span data-ttu-id="c4440-110">Exempel 1: skapa en data inblick utifrån namn</span><span class="sxs-lookup"><span data-stu-id="c4440-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c4440-111">Det första kommandot använder cmdleten Get-AzStorageAccount för att hämta lagrings kontot med namnet ContosoStorage och lagrar det sedan i $Storage variabel.</span><span class="sxs-lookup"><span data-stu-id="c4440-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c4440-112">Det andra kommandot skickar lagrings kontot i $Storage till Get-AzStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta den angivna lagrings konto och sedan lagra den i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4440-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c4440-113">Med kommandot slut skapas en inblick i lagringen med namnet MyStorageInsight på arbets ytan med namnet min.</span><span class="sxs-lookup"><span data-stu-id="c4440-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="c4440-114">Den här informationen förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="c4440-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="c4440-115">Exempel 2: skapa en inblick i lagringen med hjälp av ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="c4440-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Key1

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c4440-116">I det första kommandot används cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="c4440-116">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="c4440-117">Det andra kommandot använder cmdleten Get-AzStorageAccount för att hämta angivet lagrings konto och lagrar det sedan i $Storage-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4440-117">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c4440-118">Det tredje kommandot skickar lagrings kontot i $Storage till Get-AzStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta angiven nycklar och sedan lagra det i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4440-118">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c4440-119">Med kommandot slut skapas en insikt med namnet MyStorageInsight i arbets ytan som definieras i $Workspace.</span><span class="sxs-lookup"><span data-stu-id="c4440-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="c4440-120">Lagrings insikt förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="c4440-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="c4440-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4440-121">PARAMETERS</span></span>

### <span data-ttu-id="c4440-122">-Behållare</span><span class="sxs-lookup"><span data-stu-id="c4440-122">-Containers</span></span>
<span data-ttu-id="c4440-123">Anger listan med behållare som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="c4440-123">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4440-124">-DefaultProfile</span></span>
<span data-ttu-id="c4440-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c4440-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4440-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c4440-126">-Force</span></span>
<span data-ttu-id="c4440-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c4440-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4440-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4440-128">-Name</span></span>
<span data-ttu-id="c4440-129">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="c4440-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="c4440-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4440-130">-ResourceGroupName</span></span>
<span data-ttu-id="c4440-131">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c4440-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c4440-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4440-132">-StorageAccountKey</span></span>
<span data-ttu-id="c4440-133">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c4440-133">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c4440-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="c4440-135">Anger Azure-resursen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c4440-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="c4440-136">Det här kan hämtas genom att köra Get-AzStorageAccount cmdlet och komma åt *ID-* parametern för resultatet.</span><span class="sxs-lookup"><span data-stu-id="c4440-136">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-137">-Tabeller</span><span class="sxs-lookup"><span data-stu-id="c4440-137">-Tables</span></span>
<span data-ttu-id="c4440-138">Anger listan över tabeller som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="c4440-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="c4440-139">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c4440-139">-Workspace</span></span>
<span data-ttu-id="c4440-140">Anger arbets ytan för den nya inblicken.</span><span class="sxs-lookup"><span data-stu-id="c4440-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="c4440-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c4440-141">-WorkspaceName</span></span>
<span data-ttu-id="c4440-142">Anger namnet på en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c4440-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="c4440-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4440-143">-Confirm</span></span>
<span data-ttu-id="c4440-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4440-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4440-145">-WhatIf</span></span>
<span data-ttu-id="c4440-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4440-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4440-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4440-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4440-148">CommonParameters</span></span>
<span data-ttu-id="c4440-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4440-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4440-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4440-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4440-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4440-151">INPUTS</span></span>

### <span data-ttu-id="c4440-152">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4440-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c4440-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c4440-153">System.String</span></span>

### <span data-ttu-id="c4440-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="c4440-154">System.String[]</span></span>

## <span data-ttu-id="c4440-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4440-155">OUTPUTS</span></span>

### <span data-ttu-id="c4440-156">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c4440-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="c4440-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4440-157">NOTES</span></span>

## <span data-ttu-id="c4440-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4440-158">RELATED LINKS</span></span>

[<span data-ttu-id="c4440-159">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="c4440-159">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c4440-160">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4440-160">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


