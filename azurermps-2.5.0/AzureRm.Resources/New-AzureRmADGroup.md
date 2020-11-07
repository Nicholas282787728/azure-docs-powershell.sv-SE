---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: fa9f708355e9c2fd4df530955db1d893e7591740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930066"
---
# <span data-ttu-id="8122c-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="8122c-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="8122c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8122c-102">SYNOPSIS</span></span>
<span data-ttu-id="8122c-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="8122c-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8122c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8122c-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8122c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8122c-105">DESCRIPTION</span></span>
<span data-ttu-id="8122c-106">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="8122c-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="8122c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8122c-107">EXAMPLES</span></span>

### <span data-ttu-id="8122c-108">Exempel 1 – Skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="8122c-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="8122c-109">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och "e-postnamn" myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="8122c-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="8122c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8122c-110">PARAMETERS</span></span>

### <span data-ttu-id="8122c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8122c-111">-DefaultProfile</span></span>
<span data-ttu-id="8122c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8122c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8122c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8122c-113">-DisplayName</span></span>
<span data-ttu-id="8122c-114">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="8122c-114">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8122c-115">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="8122c-115">-MailNickname</span></span>
<span data-ttu-id="8122c-116">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="8122c-116">The mail nickname for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8122c-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8122c-117">-Confirm</span></span>
<span data-ttu-id="8122c-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8122c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8122c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8122c-119">-WhatIf</span></span>
<span data-ttu-id="8122c-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8122c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8122c-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8122c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8122c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8122c-122">CommonParameters</span></span>
<span data-ttu-id="8122c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8122c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8122c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8122c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8122c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8122c-125">INPUTS</span></span>

### <span data-ttu-id="8122c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8122c-126">System.String</span></span>

## <span data-ttu-id="8122c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8122c-127">OUTPUTS</span></span>

### <span data-ttu-id="8122c-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8122c-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8122c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8122c-129">NOTES</span></span>

## <span data-ttu-id="8122c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8122c-130">RELATED LINKS</span></span>
