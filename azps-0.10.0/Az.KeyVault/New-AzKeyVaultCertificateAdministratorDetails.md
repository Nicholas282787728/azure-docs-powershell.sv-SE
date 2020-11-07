---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922710"
---
# <span data-ttu-id="19c0b-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="19c0b-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="19c0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="19c0b-103">Skapar ett objekt för information om certifikat administratör.</span><span class="sxs-lookup"><span data-stu-id="19c0b-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="19c0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19c0b-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="19c0b-106">Cmdleten **New-AzKeyVaultCertificateAdministratorDetails** skapar ett objekt med information om hur du gör i minnet.</span><span class="sxs-lookup"><span data-stu-id="19c0b-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="19c0b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="19c0b-108">Exempel 1: skapa ett objekt med information om certifikat administratör</span><span class="sxs-lookup"><span data-stu-id="19c0b-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="19c0b-109">Det här kommandot skapar ett objekt för information om certifikat i minnet och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="19c0b-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="19c0b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19c0b-110">PARAMETERS</span></span>

### <span data-ttu-id="19c0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c0b-111">-DefaultProfile</span></span>
<span data-ttu-id="19c0b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19c0b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c0b-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="19c0b-113">-EmailAddress</span></span>
<span data-ttu-id="19c0b-114">Anger e-postadressen för certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="19c0b-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c0b-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="19c0b-115">-FirstName</span></span>
<span data-ttu-id="19c0b-116">Anger certifikat administratörens förnamn.</span><span class="sxs-lookup"><span data-stu-id="19c0b-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c0b-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="19c0b-117">-LastName</span></span>
<span data-ttu-id="19c0b-118">Anger certifikat administratörens efter namn.</span><span class="sxs-lookup"><span data-stu-id="19c0b-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c0b-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="19c0b-119">-PhoneNumber</span></span>
<span data-ttu-id="19c0b-120">Anger telefonnumret till certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="19c0b-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c0b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19c0b-121">-Confirm</span></span>
<span data-ttu-id="19c0b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19c0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c0b-123">-WhatIf</span></span>
<span data-ttu-id="19c0b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19c0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c0b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19c0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c0b-126">CommonParameters</span></span>
<span data-ttu-id="19c0b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c0b-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c0b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c0b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19c0b-129">INPUTS</span></span>

### <span data-ttu-id="19c0b-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="19c0b-130">None</span></span>
<span data-ttu-id="19c0b-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="19c0b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19c0b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19c0b-132">OUTPUTS</span></span>

### <span data-ttu-id="19c0b-133">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="19c0b-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="19c0b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19c0b-134">NOTES</span></span>

## <span data-ttu-id="19c0b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19c0b-135">RELATED LINKS</span></span>

[<span data-ttu-id="19c0b-136">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="19c0b-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

