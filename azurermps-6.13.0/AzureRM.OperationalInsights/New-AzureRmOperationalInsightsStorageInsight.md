---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 1bea5ce9eda22996eb65b6e5d26fb3af19cd1c88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576137"
---
# <span data-ttu-id="8486b-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8486b-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="8486b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8486b-102">SYNOPSIS</span></span>
<span data-ttu-id="8486b-103">Skapar en inblick i en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="8486b-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8486b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8486b-104">SYNTAX</span></span>

### <span data-ttu-id="8486b-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="8486b-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8486b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8486b-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8486b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8486b-107">DESCRIPTION</span></span>
<span data-ttu-id="8486b-108">**New-AzureRmOperationalInsightsStorageInsight-** cmdleten skapar en ny inblick i en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="8486b-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="8486b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8486b-109">EXAMPLES</span></span>

### <span data-ttu-id="8486b-110">Exempel 1: skapa en data inblick utifrån namn</span><span class="sxs-lookup"><span data-stu-id="8486b-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="8486b-111">Det första kommandot använder cmdleten Get-AzureRmStorageAccount för att hämta lagrings kontot med namnet ContosoStorage och lagrar det sedan i $Storage variabel.</span><span class="sxs-lookup"><span data-stu-id="8486b-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="8486b-112">Det andra kommandot skickar lagrings kontot i $Storage till Get-AzureRmStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta den angivna lagrings konto och sedan lagra den i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="8486b-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="8486b-113">Med kommandot slut skapas en inblick i lagringen med namnet MyStorageInsight på arbets ytan med namnet min.</span><span class="sxs-lookup"><span data-stu-id="8486b-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="8486b-114">Den här informationen förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="8486b-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="8486b-115">Exempel 2: skapa en inblick i lagringen med hjälp av ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="8486b-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="8486b-116">I det första kommandot används cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="8486b-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="8486b-117">Det andra kommandot använder cmdleten Get-AzureRmStorageAccount för att hämta angivet lagrings konto och lagrar det sedan i $Storage-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8486b-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="8486b-118">Det tredje kommandot skickar lagrings kontot i $Storage till Get-AzureRmStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta angiven nycklar och sedan lagra det i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="8486b-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="8486b-119">Med kommandot slut skapas en insikt med namnet MyStorageInsight i arbets ytan som definieras i $Workspace.</span><span class="sxs-lookup"><span data-stu-id="8486b-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="8486b-120">Lagrings insikt förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="8486b-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="8486b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8486b-121">PARAMETERS</span></span>

### <span data-ttu-id="8486b-122">-Behållare</span><span class="sxs-lookup"><span data-stu-id="8486b-122">-Containers</span></span>
<span data-ttu-id="8486b-123">Anger listan med behållare som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="8486b-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="8486b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8486b-124">-DefaultProfile</span></span>
<span data-ttu-id="8486b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8486b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8486b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8486b-126">-Force</span></span>
<span data-ttu-id="8486b-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8486b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8486b-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="8486b-128">-Name</span></span>
<span data-ttu-id="8486b-129">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="8486b-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="8486b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8486b-130">-ResourceGroupName</span></span>
<span data-ttu-id="8486b-131">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="8486b-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="8486b-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8486b-132">-StorageAccountKey</span></span>
<span data-ttu-id="8486b-133">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="8486b-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="8486b-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8486b-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="8486b-135">Anger Azure-resursen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="8486b-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="8486b-136">Det här kan hämtas genom att köra Get-AzureRmStorageAccount cmdlet och komma åt *ID-* parametern för resultatet.</span><span class="sxs-lookup"><span data-stu-id="8486b-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="8486b-137">-Tabeller</span><span class="sxs-lookup"><span data-stu-id="8486b-137">-Tables</span></span>
<span data-ttu-id="8486b-138">Anger listan över tabeller som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="8486b-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="8486b-139">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="8486b-139">-Workspace</span></span>
<span data-ttu-id="8486b-140">Anger arbets ytan för den nya inblicken.</span><span class="sxs-lookup"><span data-stu-id="8486b-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="8486b-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8486b-141">-WorkspaceName</span></span>
<span data-ttu-id="8486b-142">Anger namnet på en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="8486b-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="8486b-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8486b-143">-Confirm</span></span>
<span data-ttu-id="8486b-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8486b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8486b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8486b-145">-WhatIf</span></span>
<span data-ttu-id="8486b-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8486b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8486b-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8486b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8486b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8486b-148">CommonParameters</span></span>
<span data-ttu-id="8486b-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8486b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8486b-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8486b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8486b-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8486b-151">INPUTS</span></span>

### <span data-ttu-id="8486b-152">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8486b-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="8486b-153">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8486b-153">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="8486b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="8486b-154">System.String</span></span>

### <span data-ttu-id="8486b-155">System. string []</span><span class="sxs-lookup"><span data-stu-id="8486b-155">System.String[]</span></span>

## <span data-ttu-id="8486b-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8486b-156">OUTPUTS</span></span>

### <span data-ttu-id="8486b-157">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8486b-157">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="8486b-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8486b-158">NOTES</span></span>

## <span data-ttu-id="8486b-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8486b-159">RELATED LINKS</span></span>

[<span data-ttu-id="8486b-160">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="8486b-160">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="8486b-161">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8486b-161">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


