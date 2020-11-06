---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 61d71bebfd395b6856c93e0bc3642125437b5fe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576839"
---
# <span data-ttu-id="8b355-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8b355-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="8b355-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b355-102">SYNOPSIS</span></span>
<span data-ttu-id="8b355-103">Hämtar de aktuella åtkomst nycklarna som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8b355-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b355-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b355-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b355-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b355-105">DESCRIPTION</span></span>
<span data-ttu-id="8b355-106">Cmdleten **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** hämtar de aktuella åtkomst nycklar som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8b355-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="8b355-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b355-107">EXAMPLES</span></span>

### <span data-ttu-id="8b355-108">Exempel 1: Hämta snabb tangenter</span><span class="sxs-lookup"><span data-stu-id="8b355-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="8b355-109">Det här kommandot får åtkomst nycklar för arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8b355-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="8b355-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b355-110">PARAMETERS</span></span>

### <span data-ttu-id="8b355-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b355-111">-DefaultProfile</span></span>
<span data-ttu-id="8b355-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8b355-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b355-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b355-113">-ResourceGroupName</span></span>
<span data-ttu-id="8b355-114">Anger namnet på samlingens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8b355-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="8b355-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b355-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="8b355-116">Anger namnet på den Power BI-arbetsyta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="8b355-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8b355-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b355-117">CommonParameters</span></span>
<span data-ttu-id="8b355-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b355-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b355-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b355-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b355-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b355-120">INPUTS</span></span>

### <span data-ttu-id="8b355-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8b355-121">System.String</span></span>

## <span data-ttu-id="8b355-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b355-122">OUTPUTS</span></span>

### <span data-ttu-id="8b355-123">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="8b355-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="8b355-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b355-124">NOTES</span></span>

## <span data-ttu-id="8b355-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b355-125">RELATED LINKS</span></span>

[<span data-ttu-id="8b355-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8b355-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


