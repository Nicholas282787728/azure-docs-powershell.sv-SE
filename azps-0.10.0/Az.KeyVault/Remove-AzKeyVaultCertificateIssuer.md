---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922694"
---
# <span data-ttu-id="de657-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de657-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de657-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de657-102">SYNOPSIS</span></span>
<span data-ttu-id="de657-103">Tar bort en certifikat utfärdare från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="de657-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="de657-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de657-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de657-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de657-105">DESCRIPTION</span></span>
<span data-ttu-id="de657-106">Cmdleten **Remove-AzKeyVaultCertificateIssuer** tar bort en certifikat utfärdare från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="de657-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="de657-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de657-107">EXAMPLES</span></span>

### <span data-ttu-id="de657-108">Exempel 1: ta bort en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="de657-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="de657-109">Det här kommandot tar bort certifikat utfärdaren som heter TestIssuer01 från ContosoKV01-.</span><span class="sxs-lookup"><span data-stu-id="de657-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="de657-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de657-110">PARAMETERS</span></span>

### <span data-ttu-id="de657-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de657-111">-DefaultProfile</span></span>
<span data-ttu-id="de657-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="de657-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de657-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de657-113">-Force</span></span>
<span data-ttu-id="de657-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="de657-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de657-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="de657-115">-Name</span></span>
<span data-ttu-id="de657-116">Anger namnet på den utfärdare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="de657-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de657-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de657-117">-PassThru</span></span>
<span data-ttu-id="de657-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="de657-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de657-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="de657-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de657-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de657-120">-VaultName</span></span>
<span data-ttu-id="de657-121">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="de657-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="de657-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de657-122">-Confirm</span></span>
<span data-ttu-id="de657-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de657-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de657-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de657-124">-WhatIf</span></span>
<span data-ttu-id="de657-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de657-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de657-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de657-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de657-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de657-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de657-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de657-128">CommonParameters</span></span>
<span data-ttu-id="de657-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de657-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de657-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de657-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de657-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de657-131">INPUTS</span></span>

### <span data-ttu-id="de657-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="de657-132">None</span></span>
<span data-ttu-id="de657-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="de657-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de657-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de657-134">OUTPUTS</span></span>

### <span data-ttu-id="de657-135">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de657-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de657-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de657-136">NOTES</span></span>

## <span data-ttu-id="de657-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de657-137">RELATED LINKS</span></span>

[<span data-ttu-id="de657-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de657-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="de657-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de657-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


