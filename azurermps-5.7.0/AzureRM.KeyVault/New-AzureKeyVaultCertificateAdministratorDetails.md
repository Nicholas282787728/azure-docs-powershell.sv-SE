---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 01d0718e4efeae093b7bd9ed4fc2c6bca4cf7f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758227"
---
# <span data-ttu-id="ff242-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ff242-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="ff242-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff242-102">SYNOPSIS</span></span>
<span data-ttu-id="ff242-103">Skapar ett objekt för information om certifikat administratör.</span><span class="sxs-lookup"><span data-stu-id="ff242-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff242-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff242-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff242-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff242-105">DESCRIPTION</span></span>
<span data-ttu-id="ff242-106">Cmdleten **New-AzureKeyVaultCertificateAdministratorDetails** skapar ett objekt med information om hur du gör i minnet.</span><span class="sxs-lookup"><span data-stu-id="ff242-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="ff242-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff242-107">EXAMPLES</span></span>

### <span data-ttu-id="ff242-108">Exempel 1: skapa ett objekt med information om certifikat administratör</span><span class="sxs-lookup"><span data-stu-id="ff242-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="ff242-109">Det här kommandot skapar ett objekt för information om certifikat i minnet och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="ff242-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="ff242-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff242-110">PARAMETERS</span></span>

### <span data-ttu-id="ff242-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff242-111">-DefaultProfile</span></span>
<span data-ttu-id="ff242-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff242-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff242-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ff242-113">-EmailAddress</span></span>
<span data-ttu-id="ff242-114">Anger e-postadressen för certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="ff242-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="ff242-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ff242-115">-FirstName</span></span>
<span data-ttu-id="ff242-116">Anger certifikat administratörens förnamn.</span><span class="sxs-lookup"><span data-stu-id="ff242-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ff242-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="ff242-117">-LastName</span></span>
<span data-ttu-id="ff242-118">Anger certifikat administratörens efter namn.</span><span class="sxs-lookup"><span data-stu-id="ff242-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="ff242-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="ff242-119">-PhoneNumber</span></span>
<span data-ttu-id="ff242-120">Anger telefonnumret till certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="ff242-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="ff242-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff242-121">-Confirm</span></span>
<span data-ttu-id="ff242-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff242-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff242-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff242-123">-WhatIf</span></span>
<span data-ttu-id="ff242-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff242-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff242-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff242-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff242-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff242-126">CommonParameters</span></span>
<span data-ttu-id="ff242-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff242-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff242-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff242-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff242-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff242-129">INPUTS</span></span>

### <span data-ttu-id="ff242-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff242-130">None</span></span>
<span data-ttu-id="ff242-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ff242-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff242-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff242-132">OUTPUTS</span></span>

### <span data-ttu-id="ff242-133">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="ff242-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="ff242-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff242-134">NOTES</span></span>

## <span data-ttu-id="ff242-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff242-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff242-136">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="ff242-136">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

