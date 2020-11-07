---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: c377beb022b3d44d8b96a560c4bdd8b0c6daa387
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757772"
---
# <span data-ttu-id="cd820-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="cd820-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="cd820-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd820-102">SYNOPSIS</span></span>
<span data-ttu-id="cd820-103">Tar bort en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="cd820-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd820-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd820-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd820-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd820-105">DESCRIPTION</span></span>
<span data-ttu-id="cd820-106">Cmdleten **Remove-AzureRmPowerBIWorkspaceCollection** tar bort en Power BI-arbetsyta från din Azure-prenumeration och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cd820-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="cd820-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd820-107">EXAMPLES</span></span>

### <span data-ttu-id="cd820-108">Exempel 1: ta bort en samling med arbets ytor</span><span class="sxs-lookup"><span data-stu-id="cd820-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="cd820-109">Det här kommandot tar bort arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd820-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="cd820-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd820-110">PARAMETERS</span></span>

### <span data-ttu-id="cd820-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd820-111">-ResourceGroupName</span></span>
<span data-ttu-id="cd820-112">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="cd820-112">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="cd820-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="cd820-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="cd820-114">Anger namnet på den Power BI-arbetsyta som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cd820-114">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd820-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd820-115">-Confirm</span></span>
<span data-ttu-id="cd820-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd820-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd820-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd820-117">-WhatIf</span></span>
<span data-ttu-id="cd820-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd820-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd820-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd820-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd820-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd820-120">-DefaultProfile</span></span>
<span data-ttu-id="cd820-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd820-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd820-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd820-122">CommonParameters</span></span>
<span data-ttu-id="cd820-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd820-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd820-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd820-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd820-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd820-125">INPUTS</span></span>

## <span data-ttu-id="cd820-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd820-126">OUTPUTS</span></span>

## <span data-ttu-id="cd820-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd820-127">NOTES</span></span>

## <span data-ttu-id="cd820-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd820-128">RELATED LINKS</span></span>

[<span data-ttu-id="cd820-129">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="cd820-129">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="cd820-130">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="cd820-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


