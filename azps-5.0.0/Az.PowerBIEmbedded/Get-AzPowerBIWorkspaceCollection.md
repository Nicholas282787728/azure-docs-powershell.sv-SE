---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269252"
---
# <span data-ttu-id="d96af-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d96af-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="d96af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d96af-102">SYNOPSIS</span></span>
<span data-ttu-id="d96af-103">Hämtar Power BI-arbetsytor.</span><span class="sxs-lookup"><span data-stu-id="d96af-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="d96af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d96af-104">SYNTAX</span></span>

### <span data-ttu-id="d96af-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d96af-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d96af-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d96af-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d96af-107">DESCRIPTION</span></span>
<span data-ttu-id="d96af-108">Cmdleten **Get-AzPowerBIWorkspaceCollection** hämtar Power BI-arbetsytor i din Azure-prenumeration och resurs grupp, eller efter samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="d96af-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="d96af-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d96af-109">EXAMPLES</span></span>

### <span data-ttu-id="d96af-110">Exempel 1: Hämta alla samlingar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d96af-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="d96af-111">Det här kommandot får arbets ytans samlingar som tillhör resurs gruppen "ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="d96af-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="d96af-112">Exempel 2: Hämta en arbets yta med hjälp av dess namn</span><span class="sxs-lookup"><span data-stu-id="d96af-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="d96af-113">Det här kommandot hämtar arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d96af-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="d96af-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d96af-114">PARAMETERS</span></span>

### <span data-ttu-id="d96af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96af-115">-DefaultProfile</span></span>
<span data-ttu-id="d96af-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d96af-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d96af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96af-117">-ResourceGroupName</span></span>
<span data-ttu-id="d96af-118">Anger namnet på den resurs grupp som den här cmdleten får arbets ytans samlingar från.</span><span class="sxs-lookup"><span data-stu-id="d96af-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96af-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d96af-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="d96af-120">Anger namnet på den Power BI-arbetsyta som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d96af-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96af-121">CommonParameters</span></span>
<span data-ttu-id="d96af-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96af-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96af-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96af-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d96af-124">INPUTS</span></span>

### <span data-ttu-id="d96af-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d96af-125">System.String</span></span>

## <span data-ttu-id="d96af-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d96af-126">OUTPUTS</span></span>

### <span data-ttu-id="d96af-127">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d96af-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="d96af-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d96af-128">NOTES</span></span>

## <span data-ttu-id="d96af-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d96af-129">RELATED LINKS</span></span>

[<span data-ttu-id="d96af-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d96af-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="d96af-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="d96af-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


