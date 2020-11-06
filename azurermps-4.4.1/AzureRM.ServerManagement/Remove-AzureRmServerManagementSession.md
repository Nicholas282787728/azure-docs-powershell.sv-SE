---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577444"
---
# <span data-ttu-id="7d786-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="7d786-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="7d786-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d786-102">SYNOPSIS</span></span>
<span data-ttu-id="7d786-103">Tar bort en session med Server hantering.</span><span class="sxs-lookup"><span data-stu-id="7d786-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d786-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d786-104">SYNTAX</span></span>

### <span data-ttu-id="7d786-105">ByName</span><span class="sxs-lookup"><span data-stu-id="7d786-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d786-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="7d786-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d786-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d786-107">DESCRIPTION</span></span>
<span data-ttu-id="7d786-108">Cmdleten **Remove-AzureRmServerManagementSession** tar bort en Azure Server Management-session.</span><span class="sxs-lookup"><span data-stu-id="7d786-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="7d786-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d786-109">EXAMPLES</span></span>

## <span data-ttu-id="7d786-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d786-110">PARAMETERS</span></span>

### <span data-ttu-id="7d786-111">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="7d786-111">-NodeName</span></span>
<span data-ttu-id="7d786-112">Anger namnet på den nod där denna cmdlet tar bort sessionen.</span><span class="sxs-lookup"><span data-stu-id="7d786-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d786-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d786-114">Anger namnet på den resurs grupp som sessionen tillhör.</span><span class="sxs-lookup"><span data-stu-id="7d786-114">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="7d786-115">-Session</span><span class="sxs-lookup"><span data-stu-id="7d786-115">-Session</span></span>
<span data-ttu-id="7d786-116">Anger den session som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7d786-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="7d786-117">Den här parametern kan användas i stället för parametrarna *ResourceGroupName* , *nodnamn* och *sessionsnamn* .</span><span class="sxs-lookup"><span data-stu-id="7d786-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-118">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="7d786-118">-SessionName</span></span>
<span data-ttu-id="7d786-119">Anger namnet på den session som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7d786-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d786-120">-DefaultProfile</span></span>
<span data-ttu-id="7d786-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d786-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d786-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d786-122">CommonParameters</span></span>
<span data-ttu-id="7d786-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d786-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d786-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d786-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d786-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d786-125">INPUTS</span></span>

### <span data-ttu-id="7d786-126">Dialogsessionen</span><span class="sxs-lookup"><span data-stu-id="7d786-126">Session</span></span>
<span data-ttu-id="7d786-127">Parametern ' session ' godkänner värdet för typen session från pipeline</span><span class="sxs-lookup"><span data-stu-id="7d786-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="7d786-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d786-128">OUTPUTS</span></span>

## <span data-ttu-id="7d786-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d786-129">NOTES</span></span>

## <span data-ttu-id="7d786-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d786-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d786-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="7d786-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="7d786-132">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="7d786-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


