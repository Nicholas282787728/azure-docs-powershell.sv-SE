---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 058a914540cd03bcf523f0300e18299c3cf084ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747530"
---
# <span data-ttu-id="22f93-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22f93-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="22f93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22f93-102">SYNOPSIS</span></span>
<span data-ttu-id="22f93-103">Tar bort en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="22f93-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="22f93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22f93-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22f93-105">DESCRIPTION</span></span>
<span data-ttu-id="22f93-106">Cmdleten **Remove-AzPowerBIWorkspaceCollection** tar bort en Power BI-arbetsyta från din Azure-prenumeration och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="22f93-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="22f93-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22f93-107">EXAMPLES</span></span>

### <span data-ttu-id="22f93-108">Exempel 1: ta bort en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="22f93-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="22f93-109">Det här kommandot tar bort arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22f93-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="22f93-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22f93-110">PARAMETERS</span></span>

### <span data-ttu-id="22f93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f93-111">-DefaultProfile</span></span>
<span data-ttu-id="22f93-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="22f93-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22f93-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f93-113">-ResourceGroupName</span></span>
<span data-ttu-id="22f93-114">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="22f93-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22f93-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="22f93-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="22f93-116">Anger namnet på den Power BI-arbetsyta som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="22f93-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22f93-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22f93-117">-Confirm</span></span>
<span data-ttu-id="22f93-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22f93-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f93-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f93-119">-WhatIf</span></span>
<span data-ttu-id="22f93-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22f93-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f93-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22f93-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f93-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f93-122">CommonParameters</span></span>
<span data-ttu-id="22f93-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f93-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f93-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22f93-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f93-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22f93-125">INPUTS</span></span>

### <span data-ttu-id="22f93-126">System. String</span><span class="sxs-lookup"><span data-stu-id="22f93-126">System.String</span></span>

## <span data-ttu-id="22f93-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22f93-127">OUTPUTS</span></span>

### <span data-ttu-id="22f93-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="22f93-128">System.Void</span></span>

## <span data-ttu-id="22f93-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22f93-129">NOTES</span></span>

## <span data-ttu-id="22f93-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22f93-130">RELATED LINKS</span></span>

[<span data-ttu-id="22f93-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22f93-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="22f93-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="22f93-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


