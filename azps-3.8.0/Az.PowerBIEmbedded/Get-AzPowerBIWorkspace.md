---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088394"
---
# <span data-ttu-id="1a6bf-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="1a6bf-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="1a6bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6bf-103">Hämtar arbets ytorna i en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1a6bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a6bf-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a6bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="1a6bf-106">Cmdleten **Get-AzPowerBIWorkspace** hämtar arbets ytorna i en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1a6bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="1a6bf-108">Exempel 1: Hämta arbets ytor för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="1a6bf-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1a6bf-109">Det här kommandot får arbets ytorna som tillhör arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1a6bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a6bf-110">PARAMETERS</span></span>

### <span data-ttu-id="1a6bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6bf-111">-DefaultProfile</span></span>
<span data-ttu-id="1a6bf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1a6bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a6bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="1a6bf-114">Anger namnet på den resurs grupp som arbets ytan ska ingå i.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="1a6bf-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1a6bf-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1a6bf-116">Anger namnet på den arbets yta för vilken denna cmdlet får arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="1a6bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6bf-117">CommonParameters</span></span>
<span data-ttu-id="1a6bf-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6bf-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a6bf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6bf-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a6bf-120">INPUTS</span></span>

### <span data-ttu-id="1a6bf-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1a6bf-121">System.String</span></span>

## <span data-ttu-id="1a6bf-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a6bf-122">OUTPUTS</span></span>

### <span data-ttu-id="1a6bf-123">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1a6bf-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="1a6bf-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a6bf-124">NOTES</span></span>

## <span data-ttu-id="1a6bf-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a6bf-125">RELATED LINKS</span></span>

[<span data-ttu-id="1a6bf-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1a6bf-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


