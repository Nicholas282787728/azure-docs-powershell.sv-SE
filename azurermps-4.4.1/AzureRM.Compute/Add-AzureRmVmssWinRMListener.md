---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 77cefdacfee2e2c8cb1e0d5508a418cf6bbafcbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585784"
---
# <span data-ttu-id="c977c-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="c977c-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="c977c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c977c-102">SYNOPSIS</span></span>
<span data-ttu-id="c977c-103">Lägger till en WinRM-lyssnare till VMSS.</span><span class="sxs-lookup"><span data-stu-id="c977c-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c977c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c977c-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c977c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c977c-105">DESCRIPTION</span></span>
<span data-ttu-id="c977c-106">Cmdleten **Add-AzureRmVmssWinRMListener** lägger till en WinRM-lyssnare (Windows Remote Management) på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c977c-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c977c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c977c-107">EXAMPLES</span></span>

### <span data-ttu-id="c977c-108">Exempel 1: lägga till en WinRM-lyssnare i VMSS</span><span class="sxs-lookup"><span data-stu-id="c977c-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="c977c-109">Det här exemplet lägger till en WinRM-lyssnare till VMSS.</span><span class="sxs-lookup"><span data-stu-id="c977c-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="c977c-110">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c977c-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="c977c-111">Det andra kommandot lägger till ett HTTP-protokoll WinRM-lyssnare med certifikatet på den angivna URL-adressen till VMSS.</span><span class="sxs-lookup"><span data-stu-id="c977c-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="c977c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c977c-112">PARAMETERS</span></span>

### <span data-ttu-id="c977c-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="c977c-113">-CertificateUrl</span></span>
<span data-ttu-id="c977c-114">Anger en länk, som en URL, för det certifikat som de nya virtuella datorerna etableras med.</span><span class="sxs-lookup"><span data-stu-id="c977c-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c977c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c977c-115">-DefaultProfile</span></span>
<span data-ttu-id="c977c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c977c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c977c-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c977c-117">-Protocol</span></span>
<span data-ttu-id="c977c-118">Anger protokollet för WinRM-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="c977c-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="c977c-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c977c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c977c-120">Inkommande</span><span class="sxs-lookup"><span data-stu-id="c977c-120">Http</span></span>
- <span data-ttu-id="c977c-121">Https</span><span class="sxs-lookup"><span data-stu-id="c977c-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c977c-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c977c-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c977c-123">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="c977c-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="c977c-124">Du kan använda New-AzureRmVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="c977c-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c977c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c977c-125">-Confirm</span></span>
<span data-ttu-id="c977c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c977c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c977c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c977c-127">-WhatIf</span></span>
<span data-ttu-id="c977c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c977c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c977c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c977c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c977c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c977c-130">CommonParameters</span></span>
<span data-ttu-id="c977c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c977c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c977c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c977c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c977c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c977c-133">INPUTS</span></span>

## <span data-ttu-id="c977c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c977c-134">OUTPUTS</span></span>

### <span data-ttu-id="c977c-135">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c977c-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c977c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c977c-136">NOTES</span></span>

## <span data-ttu-id="c977c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c977c-137">RELATED LINKS</span></span>

[<span data-ttu-id="c977c-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c977c-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


