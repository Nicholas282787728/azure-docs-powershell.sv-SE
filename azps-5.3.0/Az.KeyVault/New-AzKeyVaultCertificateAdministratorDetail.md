---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524108"
---
# <span data-ttu-id="b8bb2-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="b8bb2-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="b8bb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bb2-103">Skapar ett objekt för information om certifikat administratör.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="b8bb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8bb2-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8bb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="b8bb2-106">Cmdleten **New-AzKeyVaultCertificateAdministratorDetail** skapar ett objekt med information om hur du gör i minnet.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="b8bb2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="b8bb2-108">Exempel 1: skapa ett objekt med information om certifikat administratör</span><span class="sxs-lookup"><span data-stu-id="b8bb2-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="b8bb2-109">Det här kommandot skapar ett objekt för information om certifikat i minnet och lagrar det sedan i $AdminDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="b8bb2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8bb2-110">PARAMETERS</span></span>

### <span data-ttu-id="b8bb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bb2-111">-DefaultProfile</span></span>
<span data-ttu-id="b8bb2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b8bb2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8bb2-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b8bb2-113">-EmailAddress</span></span>
<span data-ttu-id="b8bb2-114">Anger e-postadressen för certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="b8bb2-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="b8bb2-115">-FirstName</span></span>
<span data-ttu-id="b8bb2-116">Anger certifikat administratörens förnamn.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="b8bb2-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="b8bb2-117">-LastName</span></span>
<span data-ttu-id="b8bb2-118">Anger certifikat administratörens efter namn.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="b8bb2-119">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="b8bb2-119">-PhoneNumber</span></span>
<span data-ttu-id="b8bb2-120">Anger telefonnumret till certifikat administratören.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="b8bb2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8bb2-121">-Confirm</span></span>
<span data-ttu-id="b8bb2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8bb2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8bb2-123">-WhatIf</span></span>
<span data-ttu-id="b8bb2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8bb2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8bb2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bb2-126">CommonParameters</span></span>
<span data-ttu-id="b8bb2-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bb2-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8bb2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bb2-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8bb2-129">INPUTS</span></span>

### <span data-ttu-id="b8bb2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b8bb2-130">System.String</span></span>

## <span data-ttu-id="b8bb2-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8bb2-131">OUTPUTS</span></span>

### <span data-ttu-id="b8bb2-132">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="b8bb2-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="b8bb2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8bb2-133">NOTES</span></span>

## <span data-ttu-id="b8bb2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8bb2-134">RELATED LINKS</span></span>

[<span data-ttu-id="b8bb2-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="b8bb2-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

