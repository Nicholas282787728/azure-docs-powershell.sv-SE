---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747132"
---
# <span data-ttu-id="4097f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="4097f-101">New-AzADGroup</span></span>

## <span data-ttu-id="4097f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4097f-102">SYNOPSIS</span></span>
<span data-ttu-id="4097f-103">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="4097f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="4097f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4097f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4097f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4097f-105">DESCRIPTION</span></span>
<span data-ttu-id="4097f-106">Skapar en ny Active Directory-grupp.</span><span class="sxs-lookup"><span data-stu-id="4097f-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="4097f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4097f-107">EXAMPLES</span></span>

### <span data-ttu-id="4097f-108">Exempel 1 – Skapa en ny AD-grupp</span><span class="sxs-lookup"><span data-stu-id="4097f-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="4097f-109">Skapar en ny AD-grupp med namnet "MyGroupDisplayName" och e-postsmek namnet "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="4097f-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="4097f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4097f-110">PARAMETERS</span></span>

### <span data-ttu-id="4097f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4097f-111">-DefaultProfile</span></span>
<span data-ttu-id="4097f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4097f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4097f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4097f-113">-DisplayName</span></span>
<span data-ttu-id="4097f-114">Gruppens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="4097f-114">The display name for the group.</span></span>

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

### <span data-ttu-id="4097f-115">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="4097f-115">-MailNickname</span></span>
<span data-ttu-id="4097f-116">E-postsmek för gruppen.</span><span class="sxs-lookup"><span data-stu-id="4097f-116">The mail nickname for the group.</span></span> <span data-ttu-id="4097f-117">Får inte innehålla tecknet @.</span><span class="sxs-lookup"><span data-stu-id="4097f-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="4097f-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4097f-118">-Confirm</span></span>
<span data-ttu-id="4097f-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4097f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4097f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4097f-120">-WhatIf</span></span>
<span data-ttu-id="4097f-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4097f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4097f-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4097f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4097f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4097f-123">CommonParameters</span></span>
<span data-ttu-id="4097f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4097f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4097f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4097f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4097f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4097f-126">INPUTS</span></span>

### <span data-ttu-id="4097f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4097f-127">System.String</span></span>

## <span data-ttu-id="4097f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4097f-128">OUTPUTS</span></span>

### <span data-ttu-id="4097f-129">Microsoft. Azure. commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="4097f-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="4097f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4097f-130">NOTES</span></span>

## <span data-ttu-id="4097f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4097f-131">RELATED LINKS</span></span>
