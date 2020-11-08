---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262931"
---
# <span data-ttu-id="facfb-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="facfb-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="facfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="facfb-102">SYNOPSIS</span></span>
<span data-ttu-id="facfb-103">Lägger till en Key valv-nycklar i en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="facfb-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="facfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="facfb-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="facfb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="facfb-105">DESCRIPTION</span></span>
<span data-ttu-id="facfb-106">Add-AzSqlServerKeyVaultKey-cmdleten lägger till en Key valv-nycklar till den medföljande SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="facfb-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="facfb-107">Servern måste ha behörigheten get, wrapKey, unwrapKey för valvet.</span><span class="sxs-lookup"><span data-stu-id="facfb-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="facfb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="facfb-108">EXAMPLES</span></span>

### <span data-ttu-id="facfb-109">Exempel 1: Lägg till Key valv-tangenten</span><span class="sxs-lookup"><span data-stu-id="facfb-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="facfb-110">Det här kommandot lägger till Key Vault-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' på SQL Server med namnet "ContosoServer" i resurs gruppen "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="facfb-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="facfb-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="facfb-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="facfb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="facfb-112">PARAMETERS</span></span>

### <span data-ttu-id="facfb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="facfb-113">-AsJob</span></span>
<span data-ttu-id="facfb-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="facfb-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facfb-115">-DefaultProfile</span></span>
<span data-ttu-id="facfb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="facfb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="facfb-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="facfb-117">-KeyId</span></span>
<span data-ttu-id="facfb-118">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="facfb-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="facfb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="facfb-119">-ResourceGroupName</span></span>
<span data-ttu-id="facfb-120">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="facfb-120">The name of the resource group</span></span>

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

### <span data-ttu-id="facfb-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="facfb-121">-ServerName</span></span>
<span data-ttu-id="facfb-122">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="facfb-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="facfb-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="facfb-123">-Confirm</span></span>
<span data-ttu-id="facfb-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="facfb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="facfb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="facfb-125">-WhatIf</span></span>
<span data-ttu-id="facfb-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="facfb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="facfb-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="facfb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="facfb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facfb-128">CommonParameters</span></span>
<span data-ttu-id="facfb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="facfb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facfb-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="facfb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facfb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="facfb-131">INPUTS</span></span>

### <span data-ttu-id="facfb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="facfb-132">System.String</span></span>

## <span data-ttu-id="facfb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="facfb-133">OUTPUTS</span></span>

### <span data-ttu-id="facfb-134">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="facfb-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="facfb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="facfb-135">NOTES</span></span>

## <span data-ttu-id="facfb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="facfb-136">RELATED LINKS</span></span>

[<span data-ttu-id="facfb-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="facfb-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
