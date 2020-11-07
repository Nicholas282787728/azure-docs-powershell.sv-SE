---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: f00ddaade85ba981fa19209df5efb3a96160b410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755480"
---
# <span data-ttu-id="71a8e-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="71a8e-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="71a8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="71a8e-103">Hämtar Power BI-arbetsytor.</span><span class="sxs-lookup"><span data-stu-id="71a8e-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71a8e-104">SYNTAX</span></span>

### <span data-ttu-id="71a8e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="71a8e-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71a8e-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71a8e-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71a8e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="71a8e-108">Cmdleten **Get-AzureRmPowerBIWorkspaceCollection** hämtar Power BI-arbetsytor i din Azure-prenumeration och resurs grupp, eller efter samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="71a8e-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="71a8e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71a8e-109">EXAMPLES</span></span>

### <span data-ttu-id="71a8e-110">Exempel 1: Hämta alla samlingar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="71a8e-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="71a8e-111">Det här kommandot får arbets ytans samlingar som tillhör resurs gruppen "ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="71a8e-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="71a8e-112">Exempel 2: Hämta en arbets yta med hjälp av dess namn</span><span class="sxs-lookup"><span data-stu-id="71a8e-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="71a8e-113">Det här kommandot hämtar arbets ytan med namnet WCN11 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="71a8e-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="71a8e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71a8e-114">PARAMETERS</span></span>

### <span data-ttu-id="71a8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a8e-115">-DefaultProfile</span></span>
<span data-ttu-id="71a8e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="71a8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="71a8e-118">Anger namnet på den resurs grupp som den här cmdleten får arbets ytans samlingar från.</span><span class="sxs-lookup"><span data-stu-id="71a8e-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a8e-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="71a8e-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="71a8e-120">Anger namnet på den Power BI-arbetsyta som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="71a8e-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a8e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a8e-121">CommonParameters</span></span>
<span data-ttu-id="71a8e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a8e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a8e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a8e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a8e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71a8e-124">INPUTS</span></span>

### <span data-ttu-id="71a8e-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="71a8e-125">None</span></span>
<span data-ttu-id="71a8e-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="71a8e-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71a8e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71a8e-127">OUTPUTS</span></span>

### <span data-ttu-id="71a8e-128">Microsoft. Azure. commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="71a8e-128">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="71a8e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71a8e-129">NOTES</span></span>

## <span data-ttu-id="71a8e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71a8e-130">RELATED LINKS</span></span>

[<span data-ttu-id="71a8e-131">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="71a8e-131">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="71a8e-132">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="71a8e-132">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


