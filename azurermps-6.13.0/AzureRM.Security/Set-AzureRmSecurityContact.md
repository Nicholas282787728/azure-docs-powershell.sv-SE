---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576765"
---
# <span data-ttu-id="25c67-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="25c67-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="25c67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25c67-102">SYNOPSIS</span></span>
<span data-ttu-id="25c67-103">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="25c67-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25c67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25c67-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25c67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25c67-105">DESCRIPTION</span></span>
<span data-ttu-id="25c67-106">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="25c67-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="25c67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25c67-107">EXAMPLES</span></span>

### <span data-ttu-id="25c67-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25c67-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="25c67-109">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="25c67-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="25c67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25c67-110">PARAMETERS</span></span>

### <span data-ttu-id="25c67-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="25c67-111">-AlertAdmin</span></span>
<span data-ttu-id="25c67-112">Aviseringar till administratörer.</span><span class="sxs-lookup"><span data-stu-id="25c67-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c67-113">-DefaultProfile</span></span>
<span data-ttu-id="25c67-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25c67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25c67-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="25c67-115">-Email</span></span>
<span data-ttu-id="25c67-116">Postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="25c67-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c67-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="25c67-117">-Name</span></span>
<span data-ttu-id="25c67-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25c67-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c67-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="25c67-119">-NotifyOnAlert</span></span>
<span data-ttu-id="25c67-120">Aviserings aviseringar.</span><span class="sxs-lookup"><span data-stu-id="25c67-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c67-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="25c67-121">-Phone</span></span>
<span data-ttu-id="25c67-122">Telefonnr.</span><span class="sxs-lookup"><span data-stu-id="25c67-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c67-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25c67-123">-Confirm</span></span>
<span data-ttu-id="25c67-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25c67-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25c67-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25c67-125">-WhatIf</span></span>
<span data-ttu-id="25c67-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25c67-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25c67-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25c67-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25c67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c67-128">CommonParameters</span></span>
<span data-ttu-id="25c67-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c67-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c67-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c67-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25c67-131">INPUTS</span></span>

### <span data-ttu-id="25c67-132">System. String</span><span class="sxs-lookup"><span data-stu-id="25c67-132">System.String</span></span>

## <span data-ttu-id="25c67-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25c67-133">OUTPUTS</span></span>

### <span data-ttu-id="25c67-134">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="25c67-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="25c67-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25c67-135">NOTES</span></span>

## <span data-ttu-id="25c67-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25c67-136">RELATED LINKS</span></span>
