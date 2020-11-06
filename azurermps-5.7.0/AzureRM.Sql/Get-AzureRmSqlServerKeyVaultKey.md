---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 4f26955db9d99871cb0c5ae127b5977deedacf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573187"
---
# <span data-ttu-id="a5cf1-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a5cf1-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="a5cf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cf1-103">Hämtar en SQL-Servers nyckel valv nycklar.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5cf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5cf1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5cf1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cf1-106">Get-AzureRmSqlServerKeyVaultKey-cmdleten hämtar information om nyckel valv nycklar på en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="a5cf1-107">Du kan visa alla nycklar på en server eller Visa en specifik nyckel genom att ange KeyId.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="a5cf1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5cf1-108">EXAMPLES</span></span>

### <span data-ttu-id="a5cf1-109">Exempel 1: Hämta alla nyckel valv nycklar</span><span class="sxs-lookup"><span data-stu-id="a5cf1-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="a5cf1-110">Det här kommandot får alla nyckel valv nycklar på en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="a5cf1-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="a5cf1-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="a5cf1-112">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 tumavtryck: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="a5cf1-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="a5cf1-113">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="a5cf1-113">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="a5cf1-114">Det här kommandot får Key Vault-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' och lagrar det sedan i $MyServerKeyVaultKey variabel.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="a5cf1-115">Du kan kontrol lera egenskaperna för $MyServerKeyVaultKey för att få information om nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="a5cf1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5cf1-116">PARAMETERS</span></span>

### <span data-ttu-id="a5cf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf1-117">-DefaultProfile</span></span>
<span data-ttu-id="a5cf1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a5cf1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5cf1-119">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a5cf1-119">-KeyId</span></span>
<span data-ttu-id="a5cf1-120">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-120">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cf1-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5cf1-122">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a5cf1-122">The name of the resource group</span></span>

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

### <span data-ttu-id="a5cf1-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5cf1-123">-ServerName</span></span>
<span data-ttu-id="a5cf1-124">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-124">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf1-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5cf1-125">-Confirm</span></span>
<span data-ttu-id="a5cf1-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5cf1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cf1-127">-WhatIf</span></span>
<span data-ttu-id="a5cf1-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5cf1-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5cf1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cf1-130">CommonParameters</span></span>
<span data-ttu-id="a5cf1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cf1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cf1-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5cf1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cf1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5cf1-133">INPUTS</span></span>

### <span data-ttu-id="a5cf1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a5cf1-134">System.String</span></span>

## <span data-ttu-id="a5cf1-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5cf1-135">OUTPUTS</span></span>

### <span data-ttu-id="a5cf1-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="a5cf1-136">System.Object</span></span>

## <span data-ttu-id="a5cf1-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5cf1-137">NOTES</span></span>

## <span data-ttu-id="a5cf1-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5cf1-138">RELATED LINKS</span></span>

[<span data-ttu-id="a5cf1-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a5cf1-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
