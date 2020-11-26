---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271150"
---
# <span data-ttu-id="dd1c5-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="dd1c5-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="dd1c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1c5-103">Skapar en ny kommunikation för en support biljett.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="dd1c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd1c5-104">SYNTAX</span></span>

### <span data-ttu-id="dd1c5-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dd1c5-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd1c5-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd1c5-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd1c5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd1c5-107">DESCRIPTION</span></span>
<span data-ttu-id="dd1c5-108">Lägger till en ny kund kommunikation till en Azure support-biljett.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="dd1c5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd1c5-109">EXAMPLES</span></span>

### <span data-ttu-id="dd1c5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd1c5-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="dd1c5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd1c5-111">PARAMETERS</span></span>

### <span data-ttu-id="dd1c5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd1c5-112">-AsJob</span></span>
<span data-ttu-id="dd1c5-113">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-113">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-114">-Body</span><span class="sxs-lookup"><span data-stu-id="dd1c5-114">-Body</span></span>
<span data-ttu-id="dd1c5-115">Meddelande text.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c5-116">-DefaultProfile</span></span>
<span data-ttu-id="dd1c5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1c5-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd1c5-118">-Name</span></span>
<span data-ttu-id="dd1c5-119">Namn på kommunikations resursen.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-120">-Avsändare</span><span class="sxs-lookup"><span data-stu-id="dd1c5-120">-Sender</span></span>
<span data-ttu-id="dd1c5-121">Avsändarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-121">Email address of the sender.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-122">-Ämne</span><span class="sxs-lookup"><span data-stu-id="dd1c5-122">-Subject</span></span>
<span data-ttu-id="dd1c5-123">Ämne för kommunikationen.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="dd1c5-124">-SupportTicketName</span></span>
<span data-ttu-id="dd1c5-125">Namn på support ärende.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="dd1c5-126">-SupportTicketObject</span></span>
<span data-ttu-id="dd1c5-127">Objekt för support biljetter.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd1c5-128">-Confirm</span></span>
<span data-ttu-id="dd1c5-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1c5-130">-WhatIf</span></span>
<span data-ttu-id="dd1c5-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1c5-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1c5-133">CommonParameters</span></span>
<span data-ttu-id="dd1c5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1c5-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd1c5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1c5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd1c5-136">INPUTS</span></span>

### <span data-ttu-id="dd1c5-137">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="dd1c5-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="dd1c5-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd1c5-138">OUTPUTS</span></span>

### <span data-ttu-id="dd1c5-139">Microsoft. Azure. commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="dd1c5-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="dd1c5-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd1c5-140">NOTES</span></span>

## <span data-ttu-id="dd1c5-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd1c5-141">RELATED LINKS</span></span>