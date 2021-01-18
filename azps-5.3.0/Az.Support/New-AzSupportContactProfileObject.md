---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521921"
---
# <span data-ttu-id="cca2e-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="cca2e-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="cca2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cca2e-102">SYNOPSIS</span></span>
<span data-ttu-id="cca2e-103">Skapar ett profil objekt för support kontakt.</span><span class="sxs-lookup"><span data-stu-id="cca2e-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="cca2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cca2e-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cca2e-105">DESCRIPTION</span></span>
<span data-ttu-id="cca2e-106">Det här är en hjälp-cmdlet som du kan använda för att skapa ett profil objekt för support kontakt när du skapar eller uppdaterar ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="cca2e-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="cca2e-107">Du måste ange följande parametrar som är obligatoriska för att skapa ett support ärende:</span><span class="sxs-lookup"><span data-stu-id="cca2e-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="cca2e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cca2e-108">EXAMPLES</span></span>

### <span data-ttu-id="cca2e-109">Exempel 1: skapa ett kontakt objekt</span><span class="sxs-lookup"><span data-stu-id="cca2e-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="cca2e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cca2e-110">PARAMETERS</span></span>

### <span data-ttu-id="cca2e-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cca2e-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="cca2e-112">E-postadresser som listas här kommer att kopieras efter eventuell korrespondens om support ärendet.</span><span class="sxs-lookup"><span data-stu-id="cca2e-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="cca2e-113">-Country</span><span class="sxs-lookup"><span data-stu-id="cca2e-113">-Country</span></span>
<span data-ttu-id="cca2e-114">Kund land.</span><span class="sxs-lookup"><span data-stu-id="cca2e-114">Customer country.</span></span>
<span data-ttu-id="cca2e-115">Detta måste vara en giltig ISO alpha-3 landkod (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="cca2e-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="cca2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca2e-116">-DefaultProfile</span></span>
<span data-ttu-id="cca2e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cca2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca2e-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="cca2e-118">-FirstName</span></span>
<span data-ttu-id="cca2e-119">Kund förnamn.</span><span class="sxs-lookup"><span data-stu-id="cca2e-119">Customer first name.</span></span>

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

### <span data-ttu-id="cca2e-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="cca2e-120">-LastName</span></span>
<span data-ttu-id="cca2e-121">Kund efter namn.</span><span class="sxs-lookup"><span data-stu-id="cca2e-121">Customer last name.</span></span>

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

### <span data-ttu-id="cca2e-122">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="cca2e-122">-PhoneNumber</span></span>
<span data-ttu-id="cca2e-123">Kund telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="cca2e-123">Customer phone number.</span></span>
<span data-ttu-id="cca2e-124">Det här är obligatoriskt om den rekommenderade kontakt metoden är telefon.</span><span class="sxs-lookup"><span data-stu-id="cca2e-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="cca2e-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="cca2e-125">-PreferredContactMethod</span></span>
<span data-ttu-id="cca2e-126">Önskad kontakt metod.</span><span class="sxs-lookup"><span data-stu-id="cca2e-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="cca2e-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="cca2e-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="cca2e-128">Språk för kund preferens support.</span><span class="sxs-lookup"><span data-stu-id="cca2e-128">Customer preferred support language.</span></span>
<span data-ttu-id="cca2e-129">Detta måste vara ett giltigt språk för fortion för något av de språk som stöds här https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="cca2e-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="cca2e-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="cca2e-130">-PreferredTimeZone</span></span>
<span data-ttu-id="cca2e-131">Anpassad tidszon för kunder.</span><span class="sxs-lookup"><span data-stu-id="cca2e-131">Customer preferred time zone.</span></span>
<span data-ttu-id="cca2e-132">Det måste vara ett giltigt System.TimeZoneInfo.Id-värde.</span><span class="sxs-lookup"><span data-stu-id="cca2e-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="cca2e-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cca2e-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="cca2e-134">Kundens primära e-postadress.</span><span class="sxs-lookup"><span data-stu-id="cca2e-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="cca2e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cca2e-135">-Confirm</span></span>
<span data-ttu-id="cca2e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cca2e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca2e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca2e-137">-WhatIf</span></span>
<span data-ttu-id="cca2e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cca2e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cca2e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cca2e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca2e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca2e-140">CommonParameters</span></span>
<span data-ttu-id="cca2e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca2e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca2e-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cca2e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca2e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cca2e-143">INPUTS</span></span>

### <span data-ttu-id="cca2e-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="cca2e-144">None</span></span>

## <span data-ttu-id="cca2e-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cca2e-145">OUTPUTS</span></span>

### <span data-ttu-id="cca2e-146">Microsoft. Azure. commands. support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="cca2e-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="cca2e-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cca2e-147">NOTES</span></span>

## <span data-ttu-id="cca2e-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cca2e-148">RELATED LINKS</span></span>
