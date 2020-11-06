---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585292"
---
# <span data-ttu-id="f0fae-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f0fae-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f0fae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0fae-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fae-103">Lägger till en Key valv-nycklar i en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="f0fae-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0fae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0fae-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0fae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0fae-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fae-106">Add-AzureRmSqlServerKeyVaultKey-cmdleten lägger till en Key valv-nycklar till den medföljande SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="f0fae-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="f0fae-107">Servern måste ha behörigheten get, wrapKey, unwrapKey för valvet.</span><span class="sxs-lookup"><span data-stu-id="f0fae-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="f0fae-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0fae-108">EXAMPLES</span></span>

### <span data-ttu-id="f0fae-109">--------------------------Exempel 1: lägga till Key valv-tangenten--------------------------</span><span class="sxs-lookup"><span data-stu-id="f0fae-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f0fae-110">Det här kommandot lägger till Key Vault-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' på SQL Server med namnet "ContosoServer" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="f0fae-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="f0fae-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="f0fae-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="f0fae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0fae-112">PARAMETERS</span></span>

### <span data-ttu-id="f0fae-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f0fae-113">-KeyId</span></span>
<span data-ttu-id="f0fae-114">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f0fae-114">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0fae-115">-ResourceGroupName</span></span>
<span data-ttu-id="f0fae-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f0fae-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fae-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0fae-117">-ServerName</span></span>
<span data-ttu-id="f0fae-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="f0fae-118">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fae-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0fae-119">-Confirm</span></span>
<span data-ttu-id="f0fae-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0fae-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0fae-121">-WhatIf</span></span>
<span data-ttu-id="f0fae-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0fae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0fae-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0fae-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0fae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fae-124">-DefaultProfile</span></span>
<span data-ttu-id="f0fae-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0fae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fae-126">CommonParameters</span></span>
<span data-ttu-id="f0fae-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fae-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fae-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0fae-129">INPUTS</span></span>

### <span data-ttu-id="f0fae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f0fae-130">System.String</span></span>

## <span data-ttu-id="f0fae-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0fae-131">OUTPUTS</span></span>

### <span data-ttu-id="f0fae-132">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f0fae-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f0fae-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0fae-133">NOTES</span></span>

## <span data-ttu-id="f0fae-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0fae-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0fae-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f0fae-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
