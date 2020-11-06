---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584276"
---
# <span data-ttu-id="77b39-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="77b39-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="77b39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77b39-102">SYNOPSIS</span></span>
<span data-ttu-id="77b39-103">Återskapa nyckeln för en auktoriseringsregel för ett namn område.</span><span class="sxs-lookup"><span data-stu-id="77b39-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77b39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77b39-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77b39-105">DESCRIPTION</span></span>
<span data-ttu-id="77b39-106">New-AzureRmNotificationHubNamespaceKey cmdlet återskapar primär nyckeln/sekundär nyckeln för regeln för auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="77b39-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="77b39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77b39-107">EXAMPLES</span></span>

### <span data-ttu-id="77b39-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77b39-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="77b39-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="77b39-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="77b39-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77b39-110">PARAMETERS</span></span>

### <span data-ttu-id="77b39-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="77b39-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b39-112">-DefaultProfile</span></span>
<span data-ttu-id="77b39-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="77b39-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b39-114">-Force</span><span class="sxs-lookup"><span data-stu-id="77b39-114">-Force</span></span>
<span data-ttu-id="77b39-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="77b39-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-116">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="77b39-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="77b39-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77b39-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77b39-119">-Confirm</span></span>
<span data-ttu-id="77b39-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77b39-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b39-121">-WhatIf</span></span>
<span data-ttu-id="77b39-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77b39-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77b39-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77b39-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b39-124">CommonParameters</span></span>
<span data-ttu-id="77b39-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b39-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b39-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b39-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77b39-127">INPUTS</span></span>

### <span data-ttu-id="77b39-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="77b39-128">None</span></span>
<span data-ttu-id="77b39-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="77b39-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77b39-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77b39-130">OUTPUTS</span></span>

### <span data-ttu-id="77b39-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="77b39-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="77b39-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77b39-132">NOTES</span></span>

## <span data-ttu-id="77b39-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77b39-133">RELATED LINKS</span></span>

