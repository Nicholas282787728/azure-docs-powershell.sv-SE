---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930574"
---
# <span data-ttu-id="7df82-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7df82-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="7df82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7df82-102">SYNOPSIS</span></span>
<span data-ttu-id="7df82-103">Skapar ett objekt för information om certifikat administratör.</span><span class="sxs-lookup"><span data-stu-id="7df82-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7df82-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7df82-105">DESCRIPTION</span></span>
<span data-ttu-id="7df82-106">Cmdleten **New-AzureKeyVaultCertificateAdministratorDetails** skapar ett objekt med information om hur du gör i minnet.</span><span class="sxs-lookup"><span data-stu-id="7df82-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="7df82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7df82-107">EXAMPLES</span></span>

### <span data-ttu-id="7df82-108">Exempel 1: skapa ett objekt med information om certifikat administratör</span><span class="sxs-lookup"><span data-stu-id="7df82-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="7df82-109">Det här kommandot skapar ett objekt för information om certifikat i minnet och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="7df82-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="7df82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7df82-110">PARAMETERS</span></span>

### <span data-ttu-id="7df82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df82-111">-DefaultProfile</span></span>
<span data-ttu-id="7df82-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7df82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7df82-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7df82-113">-EmailAddress</span></span>
<span data-ttu-id="7df82-114">Anger e-postadressen för certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="7df82-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="7df82-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7df82-115">-FirstName</span></span>
<span data-ttu-id="7df82-116">Anger certifikat administratörens förnamn.</span><span class="sxs-lookup"><span data-stu-id="7df82-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="7df82-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="7df82-117">-LastName</span></span>
<span data-ttu-id="7df82-118">Anger certifikat administratörens efter namn.</span><span class="sxs-lookup"><span data-stu-id="7df82-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="7df82-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="7df82-119">-PhoneNumber</span></span>
<span data-ttu-id="7df82-120">Anger telefonnumret till certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="7df82-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="7df82-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7df82-121">-Confirm</span></span>
<span data-ttu-id="7df82-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7df82-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df82-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df82-123">-WhatIf</span></span>
<span data-ttu-id="7df82-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7df82-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df82-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7df82-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df82-126">CommonParameters</span></span>
<span data-ttu-id="7df82-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df82-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df82-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df82-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7df82-129">INPUTS</span></span>

## <span data-ttu-id="7df82-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7df82-130">OUTPUTS</span></span>

### <span data-ttu-id="7df82-131">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7df82-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="7df82-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7df82-132">NOTES</span></span>

## <span data-ttu-id="7df82-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7df82-133">RELATED LINKS</span></span>

[<span data-ttu-id="7df82-134">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="7df82-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

