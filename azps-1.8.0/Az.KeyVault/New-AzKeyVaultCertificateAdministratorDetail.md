---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: fb64d30618eb736434c34ae1d47059433b336779
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916305"
---
# <span data-ttu-id="ac71a-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="ac71a-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="ac71a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac71a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac71a-103">Skapar ett objekt för information om certifikat administratör.</span><span class="sxs-lookup"><span data-stu-id="ac71a-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="ac71a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac71a-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac71a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac71a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac71a-106">Cmdleten **New-AzKeyVaultCertificateAdministratorDetail** skapar ett objekt med information om hur du gör i minnet.</span><span class="sxs-lookup"><span data-stu-id="ac71a-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="ac71a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac71a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac71a-108">Exempel 1: skapa ett objekt med information om certifikat administratör</span><span class="sxs-lookup"><span data-stu-id="ac71a-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="ac71a-109">Det här kommandot skapar ett objekt för information om certifikat i minnet och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="ac71a-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="ac71a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac71a-110">PARAMETERS</span></span>

### <span data-ttu-id="ac71a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac71a-111">-DefaultProfile</span></span>
<span data-ttu-id="ac71a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ac71a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac71a-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ac71a-113">-EmailAddress</span></span>
<span data-ttu-id="ac71a-114">Anger e-postadressen för certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="ac71a-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="ac71a-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ac71a-115">-FirstName</span></span>
<span data-ttu-id="ac71a-116">Anger certifikat administratörens förnamn.</span><span class="sxs-lookup"><span data-stu-id="ac71a-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ac71a-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="ac71a-117">-LastName</span></span>
<span data-ttu-id="ac71a-118">Anger certifikat administratörens efter namn.</span><span class="sxs-lookup"><span data-stu-id="ac71a-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ac71a-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="ac71a-119">-PhoneNumber</span></span>
<span data-ttu-id="ac71a-120">Anger telefonnumret till certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="ac71a-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="ac71a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac71a-121">-Confirm</span></span>
<span data-ttu-id="ac71a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac71a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac71a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac71a-123">-WhatIf</span></span>
<span data-ttu-id="ac71a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac71a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac71a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac71a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac71a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac71a-126">CommonParameters</span></span>
<span data-ttu-id="ac71a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac71a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac71a-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac71a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac71a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac71a-129">INPUTS</span></span>

### <span data-ttu-id="ac71a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ac71a-130">System.String</span></span>

## <span data-ttu-id="ac71a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac71a-131">OUTPUTS</span></span>

### <span data-ttu-id="ac71a-132">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ac71a-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="ac71a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac71a-133">NOTES</span></span>

## <span data-ttu-id="ac71a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac71a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac71a-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="ac71a-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

