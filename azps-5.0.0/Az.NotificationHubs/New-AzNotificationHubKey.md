---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323190"
---
# <span data-ttu-id="6bb1b-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="6bb1b-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="6bb1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb1b-103">Återskapa nyckeln för en NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="6bb1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bb1b-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bb1b-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb1b-106">New-AzNotificationHubKey cmdlet återskapar primär nyckeln/sekundär nyckeln för NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="6bb1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bb1b-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb1b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6bb1b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6bb1b-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="6bb1b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6bb1b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bb1b-110">PARAMETERS</span></span>

### <span data-ttu-id="6bb1b-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6bb1b-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb1b-112">-DefaultProfile</span></span>
<span data-ttu-id="6bb1b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6bb1b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bb1b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6bb1b-114">-Force</span></span>
<span data-ttu-id="6bb1b-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6bb1b-116">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="6bb1b-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb1b-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6bb1b-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb1b-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="6bb1b-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb1b-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6bb1b-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="6bb1b-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bb1b-120">-Confirm</span></span>
<span data-ttu-id="6bb1b-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bb1b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb1b-122">-WhatIf</span></span>
<span data-ttu-id="6bb1b-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb1b-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bb1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb1b-125">CommonParameters</span></span>
<span data-ttu-id="6bb1b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb1b-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb1b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb1b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bb1b-128">INPUTS</span></span>

### <span data-ttu-id="6bb1b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6bb1b-129">System.String</span></span>

## <span data-ttu-id="6bb1b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bb1b-130">OUTPUTS</span></span>

### <span data-ttu-id="6bb1b-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6bb1b-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6bb1b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bb1b-132">NOTES</span></span>

## <span data-ttu-id="6bb1b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bb1b-133">RELATED LINKS</span></span>
