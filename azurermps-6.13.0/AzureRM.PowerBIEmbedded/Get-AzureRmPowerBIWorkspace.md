---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: 2217a6940e5f740c2499e95ff05f67c7144cbc3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755529"
---
# <span data-ttu-id="48b62-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="48b62-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="48b62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48b62-102">SYNOPSIS</span></span>
<span data-ttu-id="48b62-103">Hämtar arbets ytorna i en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="48b62-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48b62-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48b62-105">DESCRIPTION</span></span>
<span data-ttu-id="48b62-106">Cmdleten **Get-AzureRmPowerBIWorkspace** hämtar arbets ytorna i en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="48b62-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="48b62-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48b62-107">EXAMPLES</span></span>

### <span data-ttu-id="48b62-108">Exempel 1: Hämta arbets ytor för en arbets yta</span><span class="sxs-lookup"><span data-stu-id="48b62-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="48b62-109">Det här kommandot får arbets ytorna som tillhör arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="48b62-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="48b62-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48b62-110">PARAMETERS</span></span>

### <span data-ttu-id="48b62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b62-111">-DefaultProfile</span></span>
<span data-ttu-id="48b62-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="48b62-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48b62-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b62-113">-ResourceGroupName</span></span>
<span data-ttu-id="48b62-114">Anger namnet på den resurs grupp som arbets ytan ska ingå i.</span><span class="sxs-lookup"><span data-stu-id="48b62-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="48b62-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="48b62-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="48b62-116">Anger namnet på den arbets yta för vilken denna cmdlet får arbets ytor.</span><span class="sxs-lookup"><span data-stu-id="48b62-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="48b62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b62-117">CommonParameters</span></span>
<span data-ttu-id="48b62-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b62-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b62-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b62-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48b62-120">INPUTS</span></span>

### <span data-ttu-id="48b62-121">System. String</span><span class="sxs-lookup"><span data-stu-id="48b62-121">System.String</span></span>

## <span data-ttu-id="48b62-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48b62-122">OUTPUTS</span></span>

### <span data-ttu-id="48b62-123">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="48b62-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="48b62-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48b62-124">NOTES</span></span>

## <span data-ttu-id="48b62-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48b62-125">RELATED LINKS</span></span>

[<span data-ttu-id="48b62-126">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="48b62-126">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


