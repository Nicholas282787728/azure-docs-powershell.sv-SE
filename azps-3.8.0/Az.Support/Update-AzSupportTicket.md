---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089385"
---
# <span data-ttu-id="8ea67-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ea67-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="8ea67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ea67-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea67-103">Uppdaterar support ärende.</span><span class="sxs-lookup"><span data-stu-id="8ea67-103">Updates support ticket.</span></span>

## <span data-ttu-id="8ea67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ea67-104">SYNTAX</span></span>

### <span data-ttu-id="8ea67-105">UpdateByNameWithContactDetailParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8ea67-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea67-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea67-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea67-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea67-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ea67-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea67-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea67-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ea67-109">DESCRIPTION</span></span>
<span data-ttu-id="8ea67-110">Använd denna cmdlet för att uppdatera support ärendets allvarlighets nivå, status eller kund kontakt uppgifter.</span><span class="sxs-lookup"><span data-stu-id="8ea67-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="8ea67-111">Observera att det inte går att uppdatera allvarlighets graden eller status för en support biljett när biljetten kopplas till en support tekniker.</span><span class="sxs-lookup"><span data-stu-id="8ea67-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="8ea67-112">Om du vill uppdatera allvarlighets graden eller statusen efter biljett tilldelningen kontaktar du support teknikern genom att skicka en kommunikation på biljetten.</span><span class="sxs-lookup"><span data-stu-id="8ea67-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="8ea67-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ea67-113">EXAMPLES</span></span>

### <span data-ttu-id="8ea67-114">Exempel 1: uppdatera allvarlighets grad för support ärende.</span><span class="sxs-lookup"><span data-stu-id="8ea67-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8ea67-115">Exempel 2: uppdatera status för support ärende.</span><span class="sxs-lookup"><span data-stu-id="8ea67-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8ea67-116">Exempel 3: uppdatera kontakt information för support ärendet genom att ange Contact-objekt.</span><span class="sxs-lookup"><span data-stu-id="8ea67-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8ea67-117">Exempel 4: uppdatera allvarlighets graden för support biljetter via ett Ticket support-objekt.</span><span class="sxs-lookup"><span data-stu-id="8ea67-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8ea67-118">Exempel 5: uppdatera kontakt information för support ärendet genom att ange enskilda kontakt parametrar.</span><span class="sxs-lookup"><span data-stu-id="8ea67-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8ea67-119">Exempel 6: uppdatera status för support ärende via biljett objekt för support biljetter.</span><span class="sxs-lookup"><span data-stu-id="8ea67-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="8ea67-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ea67-120">PARAMETERS</span></span>

### <span data-ttu-id="8ea67-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8ea67-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="8ea67-122">Ytterligare e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="8ea67-122">Additional email addresses.</span></span>
<span data-ttu-id="8ea67-123">E-postadresser som listas här kommer att kopieras efter eventuell korrespondens om support ärendet.</span><span class="sxs-lookup"><span data-stu-id="8ea67-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="8ea67-124">-CustomerContactDetail</span></span>
<span data-ttu-id="8ea67-125">Uppdatera kontakt detaljer på SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8ea67-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="8ea67-126">-CustomerCountry</span></span>
<span data-ttu-id="8ea67-127">Kund land.</span><span class="sxs-lookup"><span data-stu-id="8ea67-127">Customer country.</span></span>
<span data-ttu-id="8ea67-128">Detta måste vara en giltig ISO alpha-3 landkod (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="8ea67-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="8ea67-129">-CustomerFirstName</span></span>
<span data-ttu-id="8ea67-130">Kund förnamn.</span><span class="sxs-lookup"><span data-stu-id="8ea67-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="8ea67-131">-CustomerLastName</span></span>
<span data-ttu-id="8ea67-132">Kund efter namn.</span><span class="sxs-lookup"><span data-stu-id="8ea67-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="8ea67-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="8ea67-134">Kund telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="8ea67-134">Customer phone number.</span></span>
<span data-ttu-id="8ea67-135">Det här är obligatoriskt om den rekommenderade kontakt metoden är telefon.</span><span class="sxs-lookup"><span data-stu-id="8ea67-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="8ea67-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="8ea67-137">Språk för kund preferens support.</span><span class="sxs-lookup"><span data-stu-id="8ea67-137">Customer preferred support language.</span></span>
<span data-ttu-id="8ea67-138">Detta måste vara ett giltigt språk för fortion för något av de språk som stöds här https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="8ea67-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="8ea67-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="8ea67-140">Anpassad tidszon för kunder.</span><span class="sxs-lookup"><span data-stu-id="8ea67-140">Customer preferred time zone.</span></span>
<span data-ttu-id="8ea67-141">Det måste vara ett giltigt System.TimeZoneInfo.Id-värde.</span><span class="sxs-lookup"><span data-stu-id="8ea67-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8ea67-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="8ea67-143">Kundens primära e-postadress.</span><span class="sxs-lookup"><span data-stu-id="8ea67-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea67-144">-DefaultProfile</span></span>
<span data-ttu-id="8ea67-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ea67-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea67-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ea67-146">-InputObject</span></span>
<span data-ttu-id="8ea67-147">SupportTicket som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="8ea67-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ea67-148">-Name</span></span>
<span data-ttu-id="8ea67-149">Namn på SupportTicket resurs som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="8ea67-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="8ea67-150">-PreferredContactMethod</span></span>
<span data-ttu-id="8ea67-151">Önskad kontakt metod.</span><span class="sxs-lookup"><span data-stu-id="8ea67-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-152">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="8ea67-152">-Severity</span></span>
<span data-ttu-id="8ea67-153">Uppdatera allvarlighets graden för SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8ea67-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-154">-Status</span><span class="sxs-lookup"><span data-stu-id="8ea67-154">-Status</span></span>
<span data-ttu-id="8ea67-155">Uppdatera status för SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="8ea67-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea67-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ea67-156">-Confirm</span></span>
<span data-ttu-id="8ea67-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ea67-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ea67-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea67-158">-WhatIf</span></span>
<span data-ttu-id="8ea67-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ea67-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ea67-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ea67-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ea67-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea67-161">CommonParameters</span></span>
<span data-ttu-id="8ea67-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea67-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea67-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ea67-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea67-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ea67-164">INPUTS</span></span>

### <span data-ttu-id="8ea67-165">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ea67-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8ea67-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ea67-166">OUTPUTS</span></span>

### <span data-ttu-id="8ea67-167">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8ea67-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8ea67-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ea67-168">NOTES</span></span>

## <span data-ttu-id="8ea67-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ea67-169">RELATED LINKS</span></span>
