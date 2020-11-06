---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575680"
---
# <span data-ttu-id="68794-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="68794-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="68794-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68794-102">SYNOPSIS</span></span>
<span data-ttu-id="68794-103">Försöker aktivera en användare hanterad Key Vault för kryptering av det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="68794-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68794-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68794-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68794-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68794-105">DESCRIPTION</span></span>
<span data-ttu-id="68794-106">Cmdleten **Enable-AzureRmDataLakeStoreKeyVault** försöker aktivera en användare hanterad Key Vault för kryptering av det angivna data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="68794-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="68794-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68794-107">EXAMPLES</span></span>

### <span data-ttu-id="68794-108">Exempel 1: Aktivera nyckelords valvet för ContosoADLS-kontot</span><span class="sxs-lookup"><span data-stu-id="68794-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="68794-109">Det här kommandot försöker aktivera den användare hanterade Key-valvet för data Lake Store-kontot med namnet ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="68794-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="68794-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68794-110">PARAMETERS</span></span>

### <span data-ttu-id="68794-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="68794-111">-Account</span></span>
<span data-ttu-id="68794-112">Kontot för data Lake Store för att aktivera hanterad gruppvalv för användare</span><span class="sxs-lookup"><span data-stu-id="68794-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68794-113">-DefaultProfile</span></span>
<span data-ttu-id="68794-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="68794-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68794-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68794-115">-ResourceGroupName</span></span>
<span data-ttu-id="68794-116">Namn på resurs gruppen som är kopplad till kontot.</span><span class="sxs-lookup"><span data-stu-id="68794-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="68794-117">Om det inte anges kommer ett försök att upptäckas.</span><span class="sxs-lookup"><span data-stu-id="68794-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="68794-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68794-118">-Confirm</span></span>
<span data-ttu-id="68794-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68794-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68794-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68794-120">-WhatIf</span></span>
<span data-ttu-id="68794-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68794-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68794-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68794-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68794-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68794-123">CommonParameters</span></span>
<span data-ttu-id="68794-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68794-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68794-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68794-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68794-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68794-126">INPUTS</span></span>

### <span data-ttu-id="68794-127">System. String</span><span class="sxs-lookup"><span data-stu-id="68794-127">System.String</span></span>

## <span data-ttu-id="68794-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68794-128">OUTPUTS</span></span>

## <span data-ttu-id="68794-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68794-129">NOTES</span></span>

## <span data-ttu-id="68794-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68794-130">RELATED LINKS</span></span>

[<span data-ttu-id="68794-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68794-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="68794-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68794-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

