---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093297"
---
# <span data-ttu-id="6bbc4-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6bbc4-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="6bbc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbc4-103">Hämtar information om Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="6bbc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bbc4-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6bbc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bbc4-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbc4-106">Cmdleten **Get-AzureSqlDatabaseServer** hämtar information om instanser av Azure SQL Database Server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="6bbc4-107">Om du anger en server med namn, returnerar denna cmdlet ett objekt som innehåller information om den servern.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="6bbc4-108">Annars returnerar cmdleten information om alla servrar.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="6bbc4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bbc4-109">EXAMPLES</span></span>

### <span data-ttu-id="6bbc4-110">Exempel 1: få information om alla servrar</span><span class="sxs-lookup"><span data-stu-id="6bbc4-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="6bbc4-111">Det här kommandot returnerar information om alla instanser av Azure SQL Database Server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="6bbc4-112">Exempel 2: Hämta information om en viss server</span><span class="sxs-lookup"><span data-stu-id="6bbc4-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="6bbc4-113">Det här kommandot returnerar information om den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="6bbc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bbc4-114">PARAMETERS</span></span>

### <span data-ttu-id="6bbc4-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="6bbc4-115">-Profile</span></span>
<span data-ttu-id="6bbc4-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bbc4-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bbc4-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6bbc4-118">-ServerName</span></span>
<span data-ttu-id="6bbc4-119">Anger namnet på den server som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="6bbc4-120">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="6bbc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbc4-121">CommonParameters</span></span>
<span data-ttu-id="6bbc4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbc4-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbc4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbc4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bbc4-124">INPUTS</span></span>

### <span data-ttu-id="6bbc4-125">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="6bbc4-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="6bbc4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bbc4-126">OUTPUTS</span></span>

### <span data-ttu-id="6bbc4-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="6bbc4-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="6bbc4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bbc4-128">NOTES</span></span>

## <span data-ttu-id="6bbc4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bbc4-129">RELATED LINKS</span></span>

[<span data-ttu-id="6bbc4-130">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="6bbc4-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6bbc4-131">List servrar</span><span class="sxs-lookup"><span data-stu-id="6bbc4-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="6bbc4-132">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="6bbc4-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6bbc4-133">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6bbc4-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="6bbc4-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6bbc4-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="6bbc4-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6bbc4-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


