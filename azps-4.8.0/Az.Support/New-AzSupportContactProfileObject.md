---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260895"
---
# <span data-ttu-id="7f5d7-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="7f5d7-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="7f5d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5d7-103">Skapar ett profil objekt för support kontakt.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="7f5d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f5d7-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f5d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5d7-106">Det här är en hjälp-cmdlet som du kan använda för att skapa ett profil objekt för support kontakt när du skapar eller uppdaterar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="7f5d7-107">Du måste ange följande parametrar som är obligatoriska för att skapa ett support ärende:</span><span class="sxs-lookup"><span data-stu-id="7f5d7-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="7f5d7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f5d7-108">EXAMPLES</span></span>

### <span data-ttu-id="7f5d7-109">Exempel 1: skapa ett kontakt objekt</span><span class="sxs-lookup"><span data-stu-id="7f5d7-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="7f5d7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f5d7-110">PARAMETERS</span></span>

### <span data-ttu-id="7f5d7-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7f5d7-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="7f5d7-112">E-postadresser som listas här kommer att kopieras efter eventuell korrespondens om support ärendet.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d7-113">-Country</span><span class="sxs-lookup"><span data-stu-id="7f5d7-113">-Country</span></span>
<span data-ttu-id="7f5d7-114">Kund land.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-114">Customer country.</span></span>
<span data-ttu-id="7f5d7-115">Detta måste vara en giltig ISO alpha-3 landkod (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="7f5d7-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="7f5d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5d7-116">-DefaultProfile</span></span>
<span data-ttu-id="7f5d7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f5d7-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7f5d7-118">-FirstName</span></span>
<span data-ttu-id="7f5d7-119">Kund förnamn.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-119">Customer first name.</span></span>

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

### <span data-ttu-id="7f5d7-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="7f5d7-120">-LastName</span></span>
<span data-ttu-id="7f5d7-121">Kund efter namn.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-121">Customer last name.</span></span>

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

### <span data-ttu-id="7f5d7-122">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="7f5d7-122">-PhoneNumber</span></span>
<span data-ttu-id="7f5d7-123">Kund telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-123">Customer phone number.</span></span>
<span data-ttu-id="7f5d7-124">Det här är obligatoriskt om den rekommenderade kontakt metoden är telefon.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="7f5d7-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="7f5d7-125">-PreferredContactMethod</span></span>
<span data-ttu-id="7f5d7-126">Önskad kontakt metod.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d7-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="7f5d7-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="7f5d7-128">Språk för kund preferens support.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-128">Customer preferred support language.</span></span>
<span data-ttu-id="7f5d7-129">Detta måste vara ett giltigt språk för fortion för något av de språk som stöds här https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="7f5d7-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="7f5d7-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="7f5d7-130">-PreferredTimeZone</span></span>
<span data-ttu-id="7f5d7-131">Anpassad tidszon för kunder.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-131">Customer preferred time zone.</span></span>
<span data-ttu-id="7f5d7-132">Det måste vara ett giltigt System.TimeZoneInfo.Id-värde.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="7f5d7-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7f5d7-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="7f5d7-134">Kundens primära e-postadress.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="7f5d7-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f5d7-135">-Confirm</span></span>
<span data-ttu-id="7f5d7-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f5d7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f5d7-137">-WhatIf</span></span>
<span data-ttu-id="7f5d7-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f5d7-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f5d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5d7-140">CommonParameters</span></span>
<span data-ttu-id="7f5d7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5d7-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f5d7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5d7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f5d7-143">INPUTS</span></span>

### <span data-ttu-id="7f5d7-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="7f5d7-144">None</span></span>

## <span data-ttu-id="7f5d7-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f5d7-145">OUTPUTS</span></span>

### <span data-ttu-id="7f5d7-146">Microsoft. Azure. commands. support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="7f5d7-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="7f5d7-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f5d7-147">NOTES</span></span>

## <span data-ttu-id="7f5d7-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f5d7-148">RELATED LINKS</span></span>
