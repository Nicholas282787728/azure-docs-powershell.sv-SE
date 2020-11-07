---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7018dc8d6951be8d1a08f4f1d1f5d615810dafab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929873"
---
# <span data-ttu-id="c273a-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c273a-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c273a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c273a-102">SYNOPSIS</span></span>
<span data-ttu-id="c273a-103">Avbryter en certifikat åtgärd i ett valv.</span><span class="sxs-lookup"><span data-stu-id="c273a-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c273a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c273a-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c273a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c273a-105">DESCRIPTION</span></span>
<span data-ttu-id="c273a-106">Cmdleten **Stop-AzureKeyVaultCertificateOperation** avbryter en certifikat åtgärd i Azure Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c273a-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="c273a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c273a-107">EXAMPLES</span></span>

### <span data-ttu-id="c273a-108">Exempel 1: avbryta en certifikat åtgärd</span><span class="sxs-lookup"><span data-stu-id="c273a-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="c273a-109">Det här kommandot avbryter TestCert02 certifikat åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c273a-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="c273a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c273a-110">PARAMETERS</span></span>

### <span data-ttu-id="c273a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c273a-111">-DefaultProfile</span></span>
<span data-ttu-id="c273a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c273a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c273a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c273a-113">-Force</span></span>
<span data-ttu-id="c273a-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c273a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c273a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c273a-115">-Name</span></span>
<span data-ttu-id="c273a-116">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="c273a-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c273a-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c273a-117">-VaultName</span></span>
<span data-ttu-id="c273a-118">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="c273a-118">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c273a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c273a-119">-Confirm</span></span>
<span data-ttu-id="c273a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c273a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c273a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c273a-121">-WhatIf</span></span>
<span data-ttu-id="c273a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c273a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c273a-123">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c273a-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c273a-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c273a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c273a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c273a-125">CommonParameters</span></span>
<span data-ttu-id="c273a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c273a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c273a-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c273a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c273a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c273a-128">INPUTS</span></span>

## <span data-ttu-id="c273a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c273a-129">OUTPUTS</span></span>

### <span data-ttu-id="c273a-130">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c273a-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="c273a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c273a-131">NOTES</span></span>

## <span data-ttu-id="c273a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c273a-132">RELATED LINKS</span></span>

[<span data-ttu-id="c273a-133">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c273a-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="c273a-134">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="c273a-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

