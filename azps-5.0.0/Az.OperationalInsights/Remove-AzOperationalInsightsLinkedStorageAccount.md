---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271309"
---
# <span data-ttu-id="e7391-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7391-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="e7391-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7391-102">SYNOPSIS</span></span>
<span data-ttu-id="e7391-103">Ta bort länkat lagrings konto för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="e7391-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e7391-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7391-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7391-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7391-105">DESCRIPTION</span></span>
<span data-ttu-id="e7391-106">Ta bort länkat lagrings konto för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="e7391-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="e7391-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7391-107">EXAMPLES</span></span>

### <span data-ttu-id="e7391-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7391-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="e7391-109">Ta bort länkat lagrings konto med Skriv "CustomLogs" för {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="e7391-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="e7391-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7391-110">PARAMETERS</span></span>

### <span data-ttu-id="e7391-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="e7391-111">-DataSourceType</span></span>
<span data-ttu-id="e7391-112">Typ av data källa ska vara en av "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="e7391-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="e7391-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7391-113">-DefaultProfile</span></span>
<span data-ttu-id="e7391-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7391-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7391-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7391-115">-Force</span></span>
<span data-ttu-id="e7391-116">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e7391-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e7391-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7391-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7391-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e7391-118">The resource group name.</span></span>

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

### <span data-ttu-id="e7391-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e7391-119">-WorkspaceName</span></span>
<span data-ttu-id="e7391-120">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="e7391-120">The workspace name.</span></span>

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

### <span data-ttu-id="e7391-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7391-121">-Confirm</span></span>
<span data-ttu-id="e7391-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7391-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7391-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7391-123">-WhatIf</span></span>
<span data-ttu-id="e7391-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7391-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7391-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7391-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7391-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7391-126">CommonParameters</span></span>
<span data-ttu-id="e7391-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7391-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7391-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7391-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7391-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7391-129">INPUTS</span></span>

### <span data-ttu-id="e7391-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7391-130">System.String</span></span>

## <span data-ttu-id="e7391-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7391-131">OUTPUTS</span></span>

### <span data-ttu-id="e7391-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7391-132">System.Boolean</span></span>

## <span data-ttu-id="e7391-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7391-133">NOTES</span></span>

## <span data-ttu-id="e7391-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7391-134">RELATED LINKS</span></span>
