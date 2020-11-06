---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573279"
---
# <span data-ttu-id="1abf9-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1abf9-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="1abf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1abf9-102">SYNOPSIS</span></span>
<span data-ttu-id="1abf9-103">Skapar en server hanterings session.</span><span class="sxs-lookup"><span data-stu-id="1abf9-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1abf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1abf9-104">SYNTAX</span></span>

### <span data-ttu-id="1abf9-105">ByName</span><span class="sxs-lookup"><span data-stu-id="1abf9-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1abf9-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="1abf9-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1abf9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1abf9-107">DESCRIPTION</span></span>
<span data-ttu-id="1abf9-108">Cmdleten **New-AzureRmServerManagementSession** skapar en Azure Server Management-session.</span><span class="sxs-lookup"><span data-stu-id="1abf9-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="1abf9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1abf9-109">EXAMPLES</span></span>

## <span data-ttu-id="1abf9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1abf9-110">PARAMETERS</span></span>

### <span data-ttu-id="1abf9-111">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="1abf9-111">-Credential</span></span>
<span data-ttu-id="1abf9-112">Anger ett **PSCredential** -objekt för anslutningen till Server hanterings sessionen.</span><span class="sxs-lookup"><span data-stu-id="1abf9-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="1abf9-113">Använd cmdleten Get-Credential för att hämta ett Credential-objekt.</span><span class="sxs-lookup"><span data-stu-id="1abf9-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1abf9-114">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1abf9-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abf9-115">-DefaultProfile</span></span>
<span data-ttu-id="1abf9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1abf9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1abf9-117">-Nod</span><span class="sxs-lookup"><span data-stu-id="1abf9-117">-Node</span></span>
<span data-ttu-id="1abf9-118">Anger den nod som den här cmdleten skapar sessionen för.</span><span class="sxs-lookup"><span data-stu-id="1abf9-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="1abf9-119">Den här parametern kan användas i stället för parametrarna *ResourceGroupName* och *nodnamn* .</span><span class="sxs-lookup"><span data-stu-id="1abf9-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="1abf9-120">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="1abf9-120">-NodeName</span></span>
<span data-ttu-id="1abf9-121">Anger namnet på den nod som den här cmdleten skapar en session för.</span><span class="sxs-lookup"><span data-stu-id="1abf9-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abf9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1abf9-122">-ResourceGroupName</span></span>
<span data-ttu-id="1abf9-123">Anger resurs gruppen för den nod som denna cmdlet skapar en session för.</span><span class="sxs-lookup"><span data-stu-id="1abf9-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="1abf9-124">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="1abf9-124">-SessionName</span></span>
<span data-ttu-id="1abf9-125">Anger det namn som ska användas för sessionen.</span><span class="sxs-lookup"><span data-stu-id="1abf9-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1abf9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abf9-126">CommonParameters</span></span>
<span data-ttu-id="1abf9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abf9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abf9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1abf9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abf9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1abf9-129">INPUTS</span></span>

### <span data-ttu-id="1abf9-130">Nodnamnet</span><span class="sxs-lookup"><span data-stu-id="1abf9-130">Node</span></span>
<span data-ttu-id="1abf9-131">Parametern ' Node ' godkänner värdet för typen nod från pipeline</span><span class="sxs-lookup"><span data-stu-id="1abf9-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="1abf9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1abf9-132">OUTPUTS</span></span>

### <span data-ttu-id="1abf9-133">Microsoft. Azure. commands. ServerManagement. Model. session</span><span class="sxs-lookup"><span data-stu-id="1abf9-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="1abf9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1abf9-134">NOTES</span></span>

## <span data-ttu-id="1abf9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1abf9-135">RELATED LINKS</span></span>

