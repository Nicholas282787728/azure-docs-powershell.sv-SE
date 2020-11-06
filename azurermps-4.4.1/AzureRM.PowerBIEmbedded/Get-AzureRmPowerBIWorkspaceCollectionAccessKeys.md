---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 387edc5f2a2fb02fb035b2090aade015573cf6d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584611"
---
# <span data-ttu-id="139ac-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="139ac-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="139ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="139ac-102">SYNOPSIS</span></span>
<span data-ttu-id="139ac-103">Hämtar de aktuella åtkomst nycklarna som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="139ac-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="139ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="139ac-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="139ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="139ac-105">DESCRIPTION</span></span>
<span data-ttu-id="139ac-106">Cmdleten **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** hämtar de aktuella åtkomst nycklar som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="139ac-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="139ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="139ac-107">EXAMPLES</span></span>

### <span data-ttu-id="139ac-108">Exempel 1: Hämta snabb tangenter</span><span class="sxs-lookup"><span data-stu-id="139ac-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="139ac-109">Det här kommandot får åtkomst nycklar för arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="139ac-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="139ac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="139ac-110">PARAMETERS</span></span>

### <span data-ttu-id="139ac-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139ac-111">-ResourceGroupName</span></span>
<span data-ttu-id="139ac-112">Anger namnet på samlingens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="139ac-112">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="139ac-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="139ac-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="139ac-114">Anger namnet på den Power BI-arbetsyta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="139ac-114">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="139ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139ac-115">-DefaultProfile</span></span>
<span data-ttu-id="139ac-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="139ac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="139ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139ac-117">CommonParameters</span></span>
<span data-ttu-id="139ac-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="139ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139ac-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139ac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139ac-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="139ac-120">INPUTS</span></span>

## <span data-ttu-id="139ac-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="139ac-121">OUTPUTS</span></span>

### <span data-ttu-id="139ac-122">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="139ac-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="139ac-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="139ac-123">NOTES</span></span>

## <span data-ttu-id="139ac-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="139ac-124">RELATED LINKS</span></span>

[<span data-ttu-id="139ac-125">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="139ac-125">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


