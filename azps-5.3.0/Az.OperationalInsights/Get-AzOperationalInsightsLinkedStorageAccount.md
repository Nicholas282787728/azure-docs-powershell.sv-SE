---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527384"
---
# <span data-ttu-id="11c2b-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11c2b-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="11c2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="11c2b-103">Hämta eller lista över länkade lagrings konton</span><span class="sxs-lookup"><span data-stu-id="11c2b-103">Get or list linked storage account</span></span>

## <span data-ttu-id="11c2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11c2b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11c2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="11c2b-106">Hämta länkat lagrings konto, lista alla länkade lagrings konton när "-DataSourceType" inte angavs</span><span class="sxs-lookup"><span data-stu-id="11c2b-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="11c2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11c2b-107">EXAMPLES</span></span>

### <span data-ttu-id="11c2b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11c2b-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="11c2b-109">lista länkade lagrings accoounts för arbets yta {arbets yta-namn}</span><span class="sxs-lookup"><span data-stu-id="11c2b-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="11c2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="11c2b-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="11c2b-111">-DataSourceType</span></span>
<span data-ttu-id="11c2b-112">Typ av data källa ska vara en av "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="11c2b-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c2b-113">-DefaultProfile</span></span>
<span data-ttu-id="11c2b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11c2b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="11c2b-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="11c2b-116">The resource group name.</span></span>

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

### <span data-ttu-id="11c2b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11c2b-117">-WorkspaceName</span></span>
<span data-ttu-id="11c2b-118">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="11c2b-118">The workspace name.</span></span>

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

### <span data-ttu-id="11c2b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c2b-119">CommonParameters</span></span>
<span data-ttu-id="11c2b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c2b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c2b-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11c2b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c2b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11c2b-122">INPUTS</span></span>

### <span data-ttu-id="11c2b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="11c2b-123">System.String</span></span>

## <span data-ttu-id="11c2b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11c2b-124">OUTPUTS</span></span>

### <span data-ttu-id="11c2b-125">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="11c2b-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="11c2b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11c2b-126">NOTES</span></span>

## <span data-ttu-id="11c2b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11c2b-127">RELATED LINKS</span></span>