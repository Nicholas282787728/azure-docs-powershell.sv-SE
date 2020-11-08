---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092185"
---
# <span data-ttu-id="37e3e-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="37e3e-101">New-AzADGroup</span></span>

## <span data-ttu-id="37e3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="37e3e-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="37e3e-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="37e3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37e3e-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37e3e-105">DESCRIPTION</span></span>
<span data-ttu-id="37e3e-106">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="37e3e-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="37e3e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37e3e-107">EXAMPLES</span></span>

### <span data-ttu-id="37e3e-108">Exempel 1 – Skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="37e3e-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="37e3e-109">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och e-postsmek namnet "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="37e3e-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="37e3e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37e3e-110">PARAMETERS</span></span>

### <span data-ttu-id="37e3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e3e-111">-DefaultProfile</span></span>
<span data-ttu-id="37e3e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37e3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e3e-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="37e3e-113">-Description</span></span>
<span data-ttu-id="37e3e-114">Beskrivning för gruppen.</span><span class="sxs-lookup"><span data-stu-id="37e3e-114">The description for the group.</span></span>

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

### <span data-ttu-id="37e3e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37e3e-115">-DisplayName</span></span>
<span data-ttu-id="37e3e-116">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="37e3e-116">The display name for the group.</span></span>

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

### <span data-ttu-id="37e3e-117">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="37e3e-117">-MailNickname</span></span>
<span data-ttu-id="37e3e-118">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="37e3e-118">The mail nickname for the group.</span></span> <span data-ttu-id="37e3e-119">Får inte innehålla tecknet @.</span><span class="sxs-lookup"><span data-stu-id="37e3e-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="37e3e-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37e3e-120">-Confirm</span></span>
<span data-ttu-id="37e3e-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37e3e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e3e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e3e-122">-WhatIf</span></span>
<span data-ttu-id="37e3e-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37e3e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e3e-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37e3e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e3e-125">CommonParameters</span></span>
<span data-ttu-id="37e3e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e3e-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37e3e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e3e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37e3e-128">INPUTS</span></span>

### <span data-ttu-id="37e3e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="37e3e-129">System.String</span></span>

## <span data-ttu-id="37e3e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37e3e-130">OUTPUTS</span></span>

### <span data-ttu-id="37e3e-131">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="37e3e-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="37e3e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37e3e-132">NOTES</span></span>

## <span data-ttu-id="37e3e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37e3e-133">RELATED LINKS</span></span>
