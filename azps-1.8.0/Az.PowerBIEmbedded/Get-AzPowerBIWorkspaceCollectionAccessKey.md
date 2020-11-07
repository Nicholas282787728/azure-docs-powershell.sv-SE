---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: b9b6092035d97aed8f70137c4157bfb80bf3f62a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747537"
---
# <span data-ttu-id="0e8b1-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="0e8b1-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="0e8b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8b1-103">Hämtar de aktuella åtkomst nycklarna som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="0e8b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e8b1-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e8b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8b1-106">Cmdleten **Get-AzPowerBIWorkspaceCollectionAccessKey** hämtar de aktuella åtkomst nycklar som är kopplade till en Power BI-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="0e8b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e8b1-107">EXAMPLES</span></span>

### <span data-ttu-id="0e8b1-108">Exempel 1: Hämta snabb tangenter</span><span class="sxs-lookup"><span data-stu-id="0e8b1-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0e8b1-109">Det här kommandot får åtkomst nycklar för arbets ytans samling med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0e8b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e8b1-110">PARAMETERS</span></span>

### <span data-ttu-id="0e8b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8b1-111">-DefaultProfile</span></span>
<span data-ttu-id="0e8b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0e8b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8b1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8b1-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e8b1-114">Anger namnet på samlingens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="0e8b1-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0e8b1-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0e8b1-116">Anger namnet på den Power BI-arbetsyta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0e8b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8b1-117">CommonParameters</span></span>
<span data-ttu-id="0e8b1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8b1-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8b1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8b1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e8b1-120">INPUTS</span></span>

### <span data-ttu-id="0e8b1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0e8b1-121">System.String</span></span>

## <span data-ttu-id="0e8b1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e8b1-122">OUTPUTS</span></span>

### <span data-ttu-id="0e8b1-123">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="0e8b1-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="0e8b1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e8b1-124">NOTES</span></span>

## <span data-ttu-id="0e8b1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e8b1-125">RELATED LINKS</span></span>

[<span data-ttu-id="0e8b1-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="0e8b1-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


