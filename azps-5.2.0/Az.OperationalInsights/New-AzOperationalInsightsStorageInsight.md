---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389817"
---
# <span data-ttu-id="4d1e7-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="4d1e7-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="4d1e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e7-103">Skapar en inblick i en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="4d1e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d1e7-104">SYNTAX</span></span>

### <span data-ttu-id="4d1e7-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="4d1e7-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d1e7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d1e7-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d1e7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d1e7-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1e7-108">**New-AzOperationalInsightsStorageInsight-** cmdleten skapar en ny inblick i en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="4d1e7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d1e7-109">EXAMPLES</span></span>

### <span data-ttu-id="4d1e7-110">Exempel 1: skapa en data inblick utifrån namn</span><span class="sxs-lookup"><span data-stu-id="4d1e7-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="4d1e7-111">Det första kommandot använder cmdleten Get-AzStorageAccount för att hämta lagrings kontot med namnet ContosoStorage och lagrar det sedan i $Storage variabel.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="4d1e7-112">Det andra kommandot skickar lagrings kontot i $Storage till Get-AzStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta den angivna lagrings konto och sedan lagra den i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="4d1e7-113">I det här exemplet hämtas den första tangenten.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-113">This example retrieves the first key.</span></span> <span data-ttu-id="4d1e7-114">Använd värdet [1] i stället för värdet [0] för att hämta den andra.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="4d1e7-115">Med kommandot slut skapas en inblick i lagringen med namnet MyStorageInsight på arbets ytan med namnet min.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="4d1e7-116">Den här informationen förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="4d1e7-117">Exempel 2: skapa en inblick i lagringen med hjälp av ett objekt i arbets ytan</span><span class="sxs-lookup"><span data-stu-id="4d1e7-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="4d1e7-118">I det första kommandot används cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och den lagras sedan i $Workspace variabel.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="4d1e7-119">Det andra kommandot använder cmdleten Get-AzStorageAccount för att hämta angivet lagrings konto och lagrar det sedan i $Storage-variabeln.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="4d1e7-120">Det tredje kommandot skickar lagrings kontot i $Storage till Get-AzStorageAccountKey-cmdlet genom att använda pipeline-operatorn för att hämta angiven nycklar och sedan lagra det i den $StorageKey variabeln.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="4d1e7-121">I det här exemplet hämtas den första tangenten.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-121">This example retrieves the first key.</span></span> <span data-ttu-id="4d1e7-122">Använd värdet [1] i stället för värdet [0] för att hämta den andra.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="4d1e7-123">Med kommandot slut skapas en insikt med namnet MyStorageInsight i arbets ytan som definieras i $Workspace.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="4d1e7-124">Lagrings insikt förbrukar data från tabellen WADWindowsEventLogsTable i den angivna lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="4d1e7-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d1e7-125">PARAMETERS</span></span>

### <span data-ttu-id="4d1e7-126">-Behållare</span><span class="sxs-lookup"><span data-stu-id="4d1e7-126">-Containers</span></span>
<span data-ttu-id="4d1e7-127">Anger listan med behållare som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="4d1e7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e7-128">-DefaultProfile</span></span>
<span data-ttu-id="4d1e7-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4d1e7-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d1e7-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4d1e7-130">-Force</span></span>
<span data-ttu-id="4d1e7-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d1e7-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d1e7-132">-Name</span></span>
<span data-ttu-id="4d1e7-133">Anger namnet på den inblickade lagringen.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="4d1e7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1e7-134">-ResourceGroupName</span></span>
<span data-ttu-id="4d1e7-135">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="4d1e7-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4d1e7-136">-StorageAccountKey</span></span>
<span data-ttu-id="4d1e7-137">Anger åtkomst tangenten för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="4d1e7-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e7-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="4d1e7-139">Anger Azure-resursen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="4d1e7-140">Det här kan hämtas genom att köra Get-AzStorageAccount cmdlet och komma åt *ID-* parametern för resultatet.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="4d1e7-141">-Tabeller</span><span class="sxs-lookup"><span data-stu-id="4d1e7-141">-Tables</span></span>
<span data-ttu-id="4d1e7-142">Anger listan över tabeller som innehåller data.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="4d1e7-143">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="4d1e7-143">-Workspace</span></span>
<span data-ttu-id="4d1e7-144">Anger arbets ytan för den nya inblicken.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="4d1e7-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d1e7-145">-WorkspaceName</span></span>
<span data-ttu-id="4d1e7-146">Anger namnet på en befintlig arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="4d1e7-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d1e7-147">-Confirm</span></span>
<span data-ttu-id="4d1e7-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1e7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1e7-149">-WhatIf</span></span>
<span data-ttu-id="4d1e7-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1e7-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1e7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e7-152">CommonParameters</span></span>
<span data-ttu-id="4d1e7-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1e7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e7-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1e7-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e7-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d1e7-155">INPUTS</span></span>

### <span data-ttu-id="4d1e7-156">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d1e7-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="4d1e7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4d1e7-157">System.String</span></span>

### <span data-ttu-id="4d1e7-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="4d1e7-158">System.String[]</span></span>

## <span data-ttu-id="4d1e7-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d1e7-159">OUTPUTS</span></span>

### <span data-ttu-id="4d1e7-160">Microsoft. Azure. commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="4d1e7-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="4d1e7-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d1e7-161">NOTES</span></span>

## <span data-ttu-id="4d1e7-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d1e7-162">RELATED LINKS</span></span>

[<span data-ttu-id="4d1e7-163">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="4d1e7-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4d1e7-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d1e7-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


