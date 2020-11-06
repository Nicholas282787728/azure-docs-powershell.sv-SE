---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: f33c6b4c7ac1fc0f1b7de11afc8395232c599539
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575518"
---
# <span data-ttu-id="87b3f-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="87b3f-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="87b3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="87b3f-103">Hämtar en eller flera noder för Server hantering.</span><span class="sxs-lookup"><span data-stu-id="87b3f-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87b3f-104">SYNTAX</span></span>

### <span data-ttu-id="87b3f-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="87b3f-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b3f-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="87b3f-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="87b3f-108">Cmdleten **Get-AzureRmServerManagementNode** har en eller flera Azure Server Management-noder.</span><span class="sxs-lookup"><span data-stu-id="87b3f-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="87b3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87b3f-109">EXAMPLES</span></span>

## <span data-ttu-id="87b3f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87b3f-110">PARAMETERS</span></span>

### <span data-ttu-id="87b3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b3f-111">-DefaultProfile</span></span>
<span data-ttu-id="87b3f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87b3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b3f-113">-Nod</span><span class="sxs-lookup"><span data-stu-id="87b3f-113">-Node</span></span>
<span data-ttu-id="87b3f-114">Anger en befintlig nod som du vill hämta *ResourceGroupName* och *nodnamn* för.</span><span class="sxs-lookup"><span data-stu-id="87b3f-114">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b3f-115">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="87b3f-115">-NodeName</span></span>
<span data-ttu-id="87b3f-116">Anger namnet på den nod som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="87b3f-116">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="87b3f-118">Anger namnet på den resurs grupp som noderna tillhör.</span><span class="sxs-lookup"><span data-stu-id="87b3f-118">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b3f-119">CommonParameters</span></span>
<span data-ttu-id="87b3f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b3f-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b3f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b3f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87b3f-122">INPUTS</span></span>

### <span data-ttu-id="87b3f-123">Nodnamnet</span><span class="sxs-lookup"><span data-stu-id="87b3f-123">Node</span></span>
<span data-ttu-id="87b3f-124">Parametern ' Node ' godkänner värdet för typen nod från pipeline</span><span class="sxs-lookup"><span data-stu-id="87b3f-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="87b3f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87b3f-125">OUTPUTS</span></span>

### <span data-ttu-id="87b3f-126">Microsoft. Azure. commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="87b3f-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="87b3f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87b3f-127">NOTES</span></span>

## <span data-ttu-id="87b3f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87b3f-128">RELATED LINKS</span></span>

[<span data-ttu-id="87b3f-129">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="87b3f-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="87b3f-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="87b3f-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


