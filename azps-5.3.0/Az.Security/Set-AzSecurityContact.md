---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525614"
---
# <span data-ttu-id="a224f-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a224f-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="a224f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a224f-102">SYNOPSIS</span></span>
<span data-ttu-id="a224f-103">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a224f-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="a224f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a224f-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a224f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a224f-105">DESCRIPTION</span></span>
<span data-ttu-id="a224f-106">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a224f-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="a224f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a224f-107">EXAMPLES</span></span>

### <span data-ttu-id="a224f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a224f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a224f-109">Uppdaterar en säkerhets kontakt för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a224f-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="a224f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a224f-110">PARAMETERS</span></span>

### <span data-ttu-id="a224f-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="a224f-111">-AlertAdmin</span></span>
<span data-ttu-id="a224f-112">Aviseringar till administratörer.</span><span class="sxs-lookup"><span data-stu-id="a224f-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="a224f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a224f-113">-DefaultProfile</span></span>
<span data-ttu-id="a224f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a224f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a224f-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="a224f-115">-Email</span></span>
<span data-ttu-id="a224f-116">Postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="a224f-116">E-Mail.</span></span>

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

### <span data-ttu-id="a224f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a224f-117">-Name</span></span>
<span data-ttu-id="a224f-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a224f-118">Resource name.</span></span>

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

### <span data-ttu-id="a224f-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="a224f-119">-NotifyOnAlert</span></span>
<span data-ttu-id="a224f-120">Aviserings aviseringar.</span><span class="sxs-lookup"><span data-stu-id="a224f-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="a224f-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="a224f-121">-Phone</span></span>
<span data-ttu-id="a224f-122">Telefonnr.</span><span class="sxs-lookup"><span data-stu-id="a224f-122">Phone.</span></span>

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

### <span data-ttu-id="a224f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a224f-123">-Confirm</span></span>
<span data-ttu-id="a224f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a224f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a224f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a224f-125">-WhatIf</span></span>
<span data-ttu-id="a224f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a224f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a224f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a224f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a224f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a224f-128">CommonParameters</span></span>
<span data-ttu-id="a224f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a224f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a224f-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a224f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a224f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a224f-131">INPUTS</span></span>

### <span data-ttu-id="a224f-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="a224f-132">None</span></span>

## <span data-ttu-id="a224f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a224f-133">OUTPUTS</span></span>

### <span data-ttu-id="a224f-134">Microsoft. Azure. commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a224f-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a224f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a224f-135">NOTES</span></span>

## <span data-ttu-id="a224f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a224f-136">RELATED LINKS</span></span>
