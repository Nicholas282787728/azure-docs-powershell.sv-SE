---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269277"
---
# <span data-ttu-id="86b96-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="86b96-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="86b96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86b96-102">SYNOPSIS</span></span>
<span data-ttu-id="86b96-103">Återskapa nyckeln för en auktoriseringsregel för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="86b96-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="86b96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86b96-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b96-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86b96-105">DESCRIPTION</span></span>
<span data-ttu-id="86b96-106">New-AzNotificationHubNamespaceKey cmdlet återskapar primär nyckeln/sekundär nyckeln för regeln för auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="86b96-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="86b96-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86b96-107">EXAMPLES</span></span>

### <span data-ttu-id="86b96-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86b96-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="86b96-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="86b96-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="86b96-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86b96-110">PARAMETERS</span></span>

### <span data-ttu-id="86b96-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="86b96-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b96-112">-DefaultProfile</span></span>
<span data-ttu-id="86b96-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="86b96-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86b96-114">-Force</span><span class="sxs-lookup"><span data-stu-id="86b96-114">-Force</span></span>
<span data-ttu-id="86b96-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="86b96-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86b96-116">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="86b96-116">-Namespace</span></span>
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

### <span data-ttu-id="86b96-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="86b96-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b96-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86b96-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="86b96-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86b96-119">-Confirm</span></span>
<span data-ttu-id="86b96-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86b96-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b96-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b96-121">-WhatIf</span></span>
<span data-ttu-id="86b96-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86b96-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b96-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86b96-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b96-124">CommonParameters</span></span>
<span data-ttu-id="86b96-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86b96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b96-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b96-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b96-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86b96-127">INPUTS</span></span>

### <span data-ttu-id="86b96-128">System. String</span><span class="sxs-lookup"><span data-stu-id="86b96-128">System.String</span></span>

## <span data-ttu-id="86b96-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86b96-129">OUTPUTS</span></span>

### <span data-ttu-id="86b96-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="86b96-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="86b96-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86b96-131">NOTES</span></span>

## <span data-ttu-id="86b96-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86b96-132">RELATED LINKS</span></span>