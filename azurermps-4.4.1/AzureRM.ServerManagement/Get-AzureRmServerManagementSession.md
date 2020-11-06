---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577475"
---
# <span data-ttu-id="24c26-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="24c26-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="24c26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24c26-102">SYNOPSIS</span></span>
<span data-ttu-id="24c26-103">Får en server hanterings session.</span><span class="sxs-lookup"><span data-stu-id="24c26-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24c26-104">SYNTAX</span></span>

### <span data-ttu-id="24c26-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="24c26-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c26-106">BySession</span><span class="sxs-lookup"><span data-stu-id="24c26-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c26-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="24c26-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24c26-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24c26-108">DESCRIPTION</span></span>
<span data-ttu-id="24c26-109">Cmdleten **Get-AzureRmServerManagementSession** får en enkel Azure Server Management-session.</span><span class="sxs-lookup"><span data-stu-id="24c26-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="24c26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24c26-110">EXAMPLES</span></span>

## <span data-ttu-id="24c26-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24c26-111">PARAMETERS</span></span>

### <span data-ttu-id="24c26-112">-Nod</span><span class="sxs-lookup"><span data-stu-id="24c26-112">-Node</span></span>
<span data-ttu-id="24c26-113">Anger ett befintligt **nodnamn** som används för att hämta parametrarna *ResourceGroupName* och *nodnamn* .</span><span class="sxs-lookup"><span data-stu-id="24c26-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="24c26-114">Du måste också ange ett värde för parametern *sessionsnamn* .</span><span class="sxs-lookup"><span data-stu-id="24c26-114">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="24c26-115">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="24c26-115">-NodeName</span></span>
<span data-ttu-id="24c26-116">Anger namnet på den nod där sessionen finns.</span><span class="sxs-lookup"><span data-stu-id="24c26-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c26-117">-ResourceGroupName</span></span>
<span data-ttu-id="24c26-118">Anger namnet på den resurs grupp som den här cmdleten hämtar sessionen för.</span><span class="sxs-lookup"><span data-stu-id="24c26-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c26-119">-Session</span><span class="sxs-lookup"><span data-stu-id="24c26-119">-Session</span></span>
<span data-ttu-id="24c26-120">Anger ett befintligt **sessionsobjekt** som används för att hämta *ResourceGroupName* , *nodnamn* och *sessionsnamn* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="24c26-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c26-121">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="24c26-121">-SessionName</span></span>
<span data-ttu-id="24c26-122">Anger namnet på den session som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="24c26-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c26-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c26-123">-DefaultProfile</span></span>
<span data-ttu-id="24c26-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24c26-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c26-125">CommonParameters</span></span>
<span data-ttu-id="24c26-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c26-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c26-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c26-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24c26-128">INPUTS</span></span>

### <span data-ttu-id="24c26-129">Nodnamnet</span><span class="sxs-lookup"><span data-stu-id="24c26-129">Node</span></span>
<span data-ttu-id="24c26-130">Parametern ' Node ' godkänner värdet för typen nod från pipeline</span><span class="sxs-lookup"><span data-stu-id="24c26-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="24c26-131">Dialogsessionen</span><span class="sxs-lookup"><span data-stu-id="24c26-131">Session</span></span>
<span data-ttu-id="24c26-132">Parametern ' session ' godkänner värdet för typen session från pipeline</span><span class="sxs-lookup"><span data-stu-id="24c26-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="24c26-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24c26-133">OUTPUTS</span></span>

### <span data-ttu-id="24c26-134">Microsoft. Azure. commands. ServerManagement. Model. session</span><span class="sxs-lookup"><span data-stu-id="24c26-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="24c26-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24c26-135">NOTES</span></span>

## <span data-ttu-id="24c26-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24c26-136">RELATED LINKS</span></span>

[<span data-ttu-id="24c26-137">Azure Server Management-cmdletar</span><span class="sxs-lookup"><span data-stu-id="24c26-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


