---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575854"
---
# <span data-ttu-id="83dac-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="83dac-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="83dac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83dac-102">SYNOPSIS</span></span>
<span data-ttu-id="83dac-103">Skapar en server hanterings session.</span><span class="sxs-lookup"><span data-stu-id="83dac-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83dac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83dac-104">SYNTAX</span></span>

### <span data-ttu-id="83dac-105">ByName</span><span class="sxs-lookup"><span data-stu-id="83dac-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83dac-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="83dac-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83dac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83dac-107">DESCRIPTION</span></span>
<span data-ttu-id="83dac-108">Cmdleten **New-AzureRmServerManagementSession** skapar en Azure Server Management-session.</span><span class="sxs-lookup"><span data-stu-id="83dac-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="83dac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83dac-109">EXAMPLES</span></span>

## <span data-ttu-id="83dac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83dac-110">PARAMETERS</span></span>

### <span data-ttu-id="83dac-111">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="83dac-111">-Credential</span></span>
<span data-ttu-id="83dac-112">Anger ett **PSCredential** -objekt för anslutningen till Server hanterings sessionen.</span><span class="sxs-lookup"><span data-stu-id="83dac-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="83dac-113">Använd cmdleten Get-Credential för att hämta ett Credential-objekt.</span><span class="sxs-lookup"><span data-stu-id="83dac-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="83dac-114">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="83dac-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83dac-115">-Nod</span><span class="sxs-lookup"><span data-stu-id="83dac-115">-Node</span></span>
<span data-ttu-id="83dac-116">Anger den nod som den här cmdleten skapar sessionen för.</span><span class="sxs-lookup"><span data-stu-id="83dac-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="83dac-117">Den här parametern kan användas i stället för parametrarna *ResourceGroupName* och *nodnamn* .</span><span class="sxs-lookup"><span data-stu-id="83dac-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83dac-118">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="83dac-118">-NodeName</span></span>
<span data-ttu-id="83dac-119">Anger namnet på den nod som den här cmdleten skapar en session för.</span><span class="sxs-lookup"><span data-stu-id="83dac-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83dac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83dac-120">-ResourceGroupName</span></span>
<span data-ttu-id="83dac-121">Anger resurs gruppen för den nod som denna cmdlet skapar en session för.</span><span class="sxs-lookup"><span data-stu-id="83dac-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dac-122">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="83dac-122">-SessionName</span></span>
<span data-ttu-id="83dac-123">Anger det namn som ska användas för sessionen.</span><span class="sxs-lookup"><span data-stu-id="83dac-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83dac-124">-DefaultProfile</span></span>
<span data-ttu-id="83dac-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83dac-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83dac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dac-126">CommonParameters</span></span>
<span data-ttu-id="83dac-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83dac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dac-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83dac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dac-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83dac-129">INPUTS</span></span>

### <span data-ttu-id="83dac-130">Nodnamnet</span><span class="sxs-lookup"><span data-stu-id="83dac-130">Node</span></span>
<span data-ttu-id="83dac-131">Parametern ' Node ' godkänner värdet för typen nod från pipeline</span><span class="sxs-lookup"><span data-stu-id="83dac-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="83dac-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83dac-132">OUTPUTS</span></span>

### <span data-ttu-id="83dac-133">Microsoft. Azure. commands. ServerManagement. Model. session</span><span class="sxs-lookup"><span data-stu-id="83dac-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="83dac-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83dac-134">NOTES</span></span>

## <span data-ttu-id="83dac-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83dac-135">RELATED LINKS</span></span>

