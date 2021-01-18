---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526153"
---
# <span data-ttu-id="b6c70-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6c70-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="b6c70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6c70-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c70-103">Försöker aktivera en användare hanterad Key Vault för kryptering av det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b6c70-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b6c70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6c70-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6c70-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c70-106">Cmdleten **Enable-AzDataLakeStoreKeyVault** försöker aktivera en användare hanterad Key Vault för kryptering av det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b6c70-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b6c70-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6c70-107">EXAMPLES</span></span>

### <span data-ttu-id="b6c70-108">Exempel 1: Aktivera nyckelords valvet för ContosoADLS-kontot</span><span class="sxs-lookup"><span data-stu-id="b6c70-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="b6c70-109">Det här kommandot försöker aktivera den användare hanterade Key-valvet för data Lake Store-kontot med namnet ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="b6c70-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="b6c70-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6c70-110">PARAMETERS</span></span>

### <span data-ttu-id="b6c70-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b6c70-111">-Account</span></span>
<span data-ttu-id="b6c70-112">Kontot för data Lake Store för att aktivera hanterad gruppvalv för användare</span><span class="sxs-lookup"><span data-stu-id="b6c70-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c70-113">-DefaultProfile</span></span>
<span data-ttu-id="b6c70-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b6c70-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c70-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6c70-116">Namn på resurs gruppen som är kopplad till kontot.</span><span class="sxs-lookup"><span data-stu-id="b6c70-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="b6c70-117">Om det inte anges kommer ett försök att upptäckas.</span><span class="sxs-lookup"><span data-stu-id="b6c70-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="b6c70-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6c70-118">-Confirm</span></span>
<span data-ttu-id="b6c70-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6c70-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c70-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c70-120">-WhatIf</span></span>
<span data-ttu-id="b6c70-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6c70-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6c70-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6c70-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c70-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c70-123">CommonParameters</span></span>
<span data-ttu-id="b6c70-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c70-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c70-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c70-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c70-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6c70-126">INPUTS</span></span>

### <span data-ttu-id="b6c70-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c70-127">System.String</span></span>

## <span data-ttu-id="b6c70-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6c70-128">OUTPUTS</span></span>

### <span data-ttu-id="b6c70-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="b6c70-129">System.Void</span></span>

## <span data-ttu-id="b6c70-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6c70-130">NOTES</span></span>

## <span data-ttu-id="b6c70-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6c70-131">RELATED LINKS</span></span>

[<span data-ttu-id="b6c70-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6c70-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6c70-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6c70-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

