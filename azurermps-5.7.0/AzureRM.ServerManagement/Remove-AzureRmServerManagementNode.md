---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755370"
---
# <span data-ttu-id="096c9-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="096c9-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="096c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="096c9-102">SYNOPSIS</span></span>
<span data-ttu-id="096c9-103">Tar bort en nod för Server hantering.</span><span class="sxs-lookup"><span data-stu-id="096c9-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="096c9-104">SYNTAX</span></span>

### <span data-ttu-id="096c9-105">ByName</span><span class="sxs-lookup"><span data-stu-id="096c9-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="096c9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="096c9-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="096c9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="096c9-107">DESCRIPTION</span></span>
<span data-ttu-id="096c9-108">Cmdleten **Remove-AzureRmServerManagementNode** tar bort en Azure Server Management-nod.</span><span class="sxs-lookup"><span data-stu-id="096c9-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="096c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="096c9-109">EXAMPLES</span></span>

## <span data-ttu-id="096c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="096c9-110">PARAMETERS</span></span>

### <span data-ttu-id="096c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096c9-111">-DefaultProfile</span></span>
<span data-ttu-id="096c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="096c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096c9-113">-Nod</span><span class="sxs-lookup"><span data-stu-id="096c9-113">-Node</span></span>
<span data-ttu-id="096c9-114">Anger den nod som denna cmdlet ska tas bort för.</span><span class="sxs-lookup"><span data-stu-id="096c9-114">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="096c9-115">Den här parametern kan användas i stället för parametrarna *ResourceGroupName* och *nodnamn* .</span><span class="sxs-lookup"><span data-stu-id="096c9-115">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="096c9-116">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="096c9-116">-NodeName</span></span>
<span data-ttu-id="096c9-117">Anger namnet på den nod som denna cmdlet ska tas bort för.</span><span class="sxs-lookup"><span data-stu-id="096c9-117">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096c9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096c9-118">-ResourceGroupName</span></span>
<span data-ttu-id="096c9-119">Anger namnet på den resurs grupp som noden tillhör.</span><span class="sxs-lookup"><span data-stu-id="096c9-119">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096c9-120">CommonParameters</span></span>
<span data-ttu-id="096c9-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096c9-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096c9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096c9-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="096c9-123">INPUTS</span></span>

### <span data-ttu-id="096c9-124">Nodnamnet</span><span class="sxs-lookup"><span data-stu-id="096c9-124">Node</span></span>
<span data-ttu-id="096c9-125">Parametern ' Node ' godkänner värdet för typen nod från pipeline</span><span class="sxs-lookup"><span data-stu-id="096c9-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="096c9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="096c9-126">OUTPUTS</span></span>

## <span data-ttu-id="096c9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="096c9-127">NOTES</span></span>

## <span data-ttu-id="096c9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="096c9-128">RELATED LINKS</span></span>

[<span data-ttu-id="096c9-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="096c9-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="096c9-130">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="096c9-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


