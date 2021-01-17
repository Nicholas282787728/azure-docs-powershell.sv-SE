---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396155"
---
# <span data-ttu-id="39432-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39432-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="39432-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39432-102">SYNOPSIS</span></span>
<span data-ttu-id="39432-103">Ange länkat lagrings konto för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="39432-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="39432-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39432-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39432-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39432-105">DESCRIPTION</span></span>
<span data-ttu-id="39432-106">Ange länkat lagrings konto för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="39432-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="39432-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39432-107">EXAMPLES</span></span>

### <span data-ttu-id="39432-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39432-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="39432-109">Ange länkad lagring för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="39432-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="39432-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39432-110">PARAMETERS</span></span>

### <span data-ttu-id="39432-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="39432-111">-DataSourceType</span></span>
<span data-ttu-id="39432-112">Typ av data källa ska vara en av "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="39432-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39432-113">-DefaultProfile</span></span>
<span data-ttu-id="39432-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39432-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39432-115">-Force</span></span>
<span data-ttu-id="39432-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="39432-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39432-117">-ResourceGroupName</span></span>
<span data-ttu-id="39432-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="39432-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="39432-119">-StorageAccountIds</span></span>
<span data-ttu-id="39432-120">lista över lagrings konto-ID.</span><span class="sxs-lookup"><span data-stu-id="39432-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39432-121">-WorkspaceName</span></span>
<span data-ttu-id="39432-122">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="39432-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39432-123">-Confirm</span></span>
<span data-ttu-id="39432-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39432-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39432-125">-WhatIf</span></span>
<span data-ttu-id="39432-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39432-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39432-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39432-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39432-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39432-128">CommonParameters</span></span>
<span data-ttu-id="39432-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39432-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39432-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39432-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39432-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39432-131">INPUTS</span></span>

### <span data-ttu-id="39432-132">System. String</span><span class="sxs-lookup"><span data-stu-id="39432-132">System.String</span></span>

## <span data-ttu-id="39432-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39432-133">OUTPUTS</span></span>

### <span data-ttu-id="39432-134">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="39432-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="39432-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39432-135">NOTES</span></span>

## <span data-ttu-id="39432-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39432-136">RELATED LINKS</span></span>
